# digioh-android-sdk!

## Digioh android SDK Integration
To add `Digioh.aar` to your android project follow below instructions:
- Download `Digioh.aar` from this repo.
- Open your android project and drag the `Digioh.aar` under libs in Project > app. As shown in below image.
- Open app level `build.gradle` and add the following lines in `dependencies`
```
implementation 'com.squareup.okhttp3:okhttp:4.10.0'
implementation 'com.google.code.gson:gson:2.10.1'
implementation fileTree(dir: 'libs', include: ['.jar', '.aar'])
implementation files("libs/Digioh.aar")
```
- Sync Gradle files
- `import com.digioh.Digioh` to use.

Refer to the image below for further guidance on the steps.

![android Digioh](https://user-images.githubusercontent.com/58115993/236550128-d061fd2a-db84-4502-9a18-cd302af1f77f.gif)

## How to get `Digioh Boxes`
```
val digioh = Digioh(userGId = "Your Api Key")
digioh.checkShowBoxes(params: String?,context: Context, callback:  (List<Int>?, Error?) -> Unit)
```
- params if any pass in string otherwise `"" or null`
- `context` pass `activity context`
- will return `List` with boxes `id`

## Present `Digioh Boxes` in `Web View`
``
digioh.showBox(boxId: Int,context: Context)
``
- pass box `ID`
- pass `activiy context`
