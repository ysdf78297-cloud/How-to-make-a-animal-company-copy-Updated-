# Clone OG Animal Company (Xera Backend)

CREDITS:

Xera - Developer  
1. Install Base APK & Gamedata
- Use QuestAppVersionSwitcher to get target APK version
- Go to the /gamedata folder in this repo and download the wanted game data

2. Decompile APK
- Use APKToolGUI or similar to unpack

3. Patch Server URL
- Open global-metadata.dat in MetaDataStringEditor
- Ctrl+F:
  https://animalcompany.us-east1.nakamacloud.io
- Replace with:
  https://ac-xerabackend.pythonanywhere.com or your hosted backend url if self hosting
  - Save it but add a 1 at the start (Some you have to put .dat At the end added if it isn't there)
  - Delete the old metadata
  - Rename the new metadata and delete the 1

- Or go to /native-lib patch native-lib.cpp for your url and recompile (THIS IS THE ONLY WAY TO DO IT ON NEWER VERSIONS PAST LAVA)

4. Inject App ID
- Open assets/bin/data/globalgamemanagers in UABEA
- Ctrl+F: OculusPlatformSettings ? Extract as raw
- Find the strings example : bd67a80c08d994c8eb6ebcb4e1e67891
- Search it up with File Explorer in \assets\bin\Data
- Edit that (Open in HxD)
- Replace Meta App ID with your own from developer.oculus.com

5. Rebrand Package Name
- Change:
  woosterGames.animalCompany
- Edit in AndroidManifest.xml and apktool.yml

6. Upload to Meta
- Sign in to developer.oculus.com
- Build and sign APK
- Upload to App Lab

7. Submissions
- On meta find data-use-checkup
- Activate these submissions User ID User profile User age group
- Submit it
- It should say activate beside them
