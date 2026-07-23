# Angavu MES — installable app

Same pattern as Angavu POS: a tiny launcher hosted free on
GitHub Pages that installs like a real app and opens the live
MES (which runs inside your Apps Script project, same
spreadsheet as the POS).

## Before hosting
1. Apply the 3-edit patch to Code.gs described in
   CODE_GS_PATCH_INSTRUCTIONS.txt (adds MES roles + routing).
2. Add MES_SchemaSetup.gs, MES_Code.gs, and MesIndex.html to the
   same Apps Script project as the POS. Run installMESSchema once.
3. Deploy -> Manage deployments -> New version.
4. Edit index.html here: replace the href on the gold button
   with YOUR /exec URL + "?app=mes" (keep the query string).

## Host on GitHub Pages (new repo, e.g. "angavu-mes")
1. github.com -> New repository -> angavu-mes -> Public -> Create
2. Upload these 5 files: index.html, manifest.json, sw.js,
   icon-192.png, icon-512.png, icon-512-maskable.png
3. Settings -> Pages -> Branch: main, folder: / (root) -> Save
4. Your app URL appears at the top after ~2 minutes.

## Install on devices
Android (Chrome): open the URL -> "Install app".
iPad/iPhone (Safari): Share -> Add to Home Screen.
First launch may need a one-time Google sign-in if the screen
is blank — same behaviour as the POS app.
