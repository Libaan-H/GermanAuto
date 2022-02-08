**Getting set up:** (in minutes)

1. Make sure you have the Firebase CLI installed. Create a new project in the Firebase console and **make sure** you go into project settings and choose a GCP resource location under the general tab.
2. Enable Facebook, Google, and Email/Password authentication in the Firebase console. When enabling "Email/Password", be sure to enable "Email link" as well. (OAuth with Facebook and Google will require some additional steps, outlined when you view each method in the Firebase authentication console)
3. Clone the project and `npm run setup`.
4. Select your Firebase project in the command line by using `firebase use [YOUR_PROJECT_ID]`.
5. Add your Firebase keys to `.env.development.local` and `.env.production.local`.
6. Go into `public/firebase-messaging-sw.js` and manually change the messagingSenderId, which will be the same as `REACT_APP_FIREBASE_MESSAGING_ID` in your `.env` files.
7. Run `npm run build` to create a production build of your project, and `firebase deploy`. Your application should now be hosted and ready to visit.
