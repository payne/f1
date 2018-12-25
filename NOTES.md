
## FireStore Security

```
https://matt-f1.firebaseapp.com/notes
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read: if request.auth.uid != null;
      allow write: if request.auth.uid != null;
    }
  }
}
```
