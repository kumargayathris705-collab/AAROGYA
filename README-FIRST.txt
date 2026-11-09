AAROGYA FIREBASE PREVIEW

Contents
- index.html: AAROGYA app using Firebase Authentication + Cloud Firestore.
- firestore.rules: security rules for profiles, User medication data, one-time invitations, and authorised Caretaker links.
- manifest.webmanifest, service-worker.js, icons, and logo: existing PWA assets.

IMPORTANT
This is a preview integration. It has passed a JavaScript syntax check, but has NOT been exercised against your live Firebase project or tested with the Firebase Emulator. Do not enter real medical information until the rules and account/link flows have been tested.

Firebase project configured in this build: aarogya-46b1d
Authentication: Email/Password
Firestore region: asia-south1 (Mumbai)

NEXT SETUP
1. In Firebase Console, open Firestore Database -> Rules.
2. Replace the rules with the complete contents of firestore.rules and click Publish.
3. Deploy the contents of this ZIP folder to your Netlify site (index.html must be at the site root).
4. Test using dummy accounts first: create one User account and one Caretaker account with different email addresses. Sign in as the User, open Care, create an invitation code, then sign in as the Caretaker and accept that code.

Do not loosen the Firestore rules to public read/write. Keep a backup of the previous Netlify deployment so you can roll back.

DATA NOTE
The previous username/PIN localStorage accounts are not automatically migrated into Firebase. This build creates new Email/Password accounts. Old local data is not intentionally erased by this package, but it is not imported into the cloud.


INSTALL ON ANDROID
1. Deploy this folder to your HTTPS website (Netlify is suitable).
2. Open the website in Chrome on Android.
3. Open the browser menu and choose Install app or Add to Home screen.

INSTALL ON iPHONE / iPAD
1. Deploy this folder to your HTTPS website.
2. Open the website in Safari.
3. Tap Share -> Add to Home Screen -> Add.
   iOS installs this as a Home Screen web app (PWA), not through the App Store.

The app must be hosted on HTTPS for installation and service-worker support.
The interface keeps the app shell within one screen; longer lists scroll inside
their own content area. The Firebase preview still requires the setup and dummy
account testing described above before real medical data is entered.
