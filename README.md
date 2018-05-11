# firebase-functions-helper
A helper NPM package for Firebase Cloud Functions

## Installation 

Install using [__npm__](https://www.npmjs.com/).

```sh
npm install firebase-functions-helper
```

## Get Google Cloud Account Credentials from Firebase

You can __Generate New Private Key__ from Project Settings from [Firebase Console](https://console.firebase.google.com).

After that you need to copy the __databaseURL__ for initiating the App. 

## Usage 

### Initialize Firebase App

This is the first step that you need to do before doing any other actions.

```
const firebaseFunctionsHelper = require('firebase-functions-helper');
const serviceAccount = require('./serviceAccountKey.json');

// Initialize Firebase App
firebaseFunctionsHelper.initializeApp(serviceAccount, databaseURL);
```

### Get Firestore Collection with Sub Collection

```
// Start exporting your collection
var result = firebaseFunctionsHelper.backup('collection-name', 'sub-collection-optional');
result.then(data => console.log(data))
```

## Contributions

This project is based on [firebase-functions-snippets](https://github.com/dalenguyen/firebase-functions-snippets), feel free to report bugs and make feature requests in the [Issue Tracker](https://github.com/dalenguyen/firebase-functions-helper/issues), fork and create pull requests!