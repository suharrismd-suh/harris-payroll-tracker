# HARRIS payroll tracker

Static payroll tracker ready for GitHub Pages hosting with optional Firebase Firestore live sync.

## Files

- `HARRIS payroll tracker.html`: main app
- `index.html`: GitHub Pages entry point
- `firebase-config.js`: Firebase project settings to fill in
- `firestore.rules`: starter Firestore rules

## GitHub Pages setup

1. Create a GitHub repository.
2. Upload all files in this folder.
3. In GitHub, open `Settings` -> `Pages`.
4. Set the source to deploy from the main branch root.
5. GitHub Pages will publish a site URL.

## Firebase setup

1. Create a Firebase project.
2. Enable Firestore Database.
3. Enable Firebase Authentication and turn on the `Anonymous` sign-in provider.
4. In Project Settings, create a Web App and copy the config values.
5. Paste those values into `firebase-config.js`.
6. In Firestore Rules, start with `firestore.rules`.

## Shared usage

- Open the GitHub Pages URL.
- The app stores shared data in the Firestore document `trackers/<workspace-id>`.
- The workspace id comes from the URL query string: `?workspace=corina-elgart-timesheet`
- Use the app's `Copy Share Link` button and send that link to Corina.

## Important note

The app signs users in anonymously so Corina does not need a password. Anyone with the shared link can still access that workspace, so treat the link as private.
