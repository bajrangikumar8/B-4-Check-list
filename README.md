# 104 Room Checklist – Multi Mobile Live Version

This version keeps a local copy on each phone and synchronizes all phones through Firebase Realtime Database. It supports 5+ phones.

## One-time setup
1. Create a Firebase project: https://console.firebase.google.com/
2. Add a Web app.
3. Enable Authentication > Sign-in method > Anonymous.
4. Create Realtime Database.
5. For initial setup, use these Realtime Database Rules (authenticated users only):

{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}

6. Copy the Web app `firebaseConfig` into `firebase-config.js`.
7. Upload/replace all files in GitHub Pages.

The cloud database is the shared source for live sync; each phone also keeps a local offline copy.


## Building structure
- Building 2: 88 rooms (22 per floor)
- Building 3: Part A 52 rooms (13 per floor), Part B 64 rooms (16 per floor), Part C 52 rooms (13 per floor)
- Building 4: 104 rooms (26 per floor)
Total: 360 rooms. Building 3 contains Parts A/B/C.


## Building structure
Building 2: 88 rooms. Building 3 contains Part A (52), Part B (64), Part C (52). Building 4: 104 rooms. Total 360 rooms.
