# Banker's Guarantee

## Table of contents

- [Introduction](#introduction)
- [Initial Set Up](#how-to-setup)

  - [Generate Affinidi API Key](#generate-api-key)
  - [Firebase Credentials](#firebase)
  - [Configure .env File](#configure-.env-file)

- [How to run](#how-to-run)
  - [Sequence](#sequence)

## Introduction

In this application, the business owner applies for the Banker's guarantee which can be given to the Client as a financial security since it ensures the payment recovery even if the business owner fails to make the payment after the deal.

You can either run this program in your local machine or try it out here: http://applicant.verifiable-credential.tech/

## Initial Set Up

### Generate API Key

Before you could use our API and SDK services, you would have to register to get the API keys.

1. Go to apikey.affinidi.com
2. Register for an account
3. Store the `API Key` and `API Key Hash` safely

### Firebase

We will be using firebase to mimic issuer's database which stores all of the applications.

1. Go to Firebase Console https://console.firebase.google.com/
2. Create a new Firestore
3. Navigation to Project Settings
4. Look for `firebaseConfig` and copy the credentials. It should look like

```
  var firebaseConfig = {
    apiKey: <<SOME API KEY>>,
    authDomain: "<<SOMEP PROJECT NAME>>.firebaseapp.com",
    projectId: "<<SOMEP PROJECT NAME>>",
    storageBucket: "<<SOMEP PROJECT NAME>>.appspot.com",
    messagingSenderId: <<SOME STRING>>,
    appId: <<SOME STRING>>
  };
```

### Configure .env file

1. Open terminal and navigate to the project folder
2. Run `cp .env.example .env`
3. Fill in the .env file with the details that you have gathered in the previous steps

```
REACT_APP_API_KEY=<<Afffinidi's API Key>>
REACT_APP_API_KEY_HASH=<<Affinidi's API Key Hash>>
REACT_APP_ENVIRONMENT=prod
REACT_APP_WALLET_URL=<<URL OF THE WALLET APPLICATION>>

REACT_APP_FIREBASE_API_KEY=<<Firebase's apiKey>>
REACT_APP_FIREBASE_AUTHDOMAIN=<<Firebase's authDomain>>
REACT_APP_FIREBASE_PROJECT_ID=<<Firebase's projectId>>
REACT_APP_FIREBASE_STORAGEBUCKET=<<Firebase's storageBucket>>
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=<<Firebase's messagingSenderId>>
REACT_APP_FIREBASE_APP_ID=<<Firebase's appId>>
```

## How to run

1. Open terminal and navigate to the project folder
2. Run `npm install`
3. Run `cp .env.example .env`
4. Populate the credentials in `.env`
5. Run `npm start`
