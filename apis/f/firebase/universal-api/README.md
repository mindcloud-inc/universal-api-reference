# <img src="https://images.mindcloud.co/apps/icons/firebase_1776870642085.png" alt="Firebase logo" width="28" height="28"> Firebase: Universal API

Manage Firebase projects and Firebase Android, iOS, and web app resources through the Firebase Management API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/firebase/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://firebase.google.com
- **Vendor API docs:** https://firebase.google.com/docs/reference/firebase-management/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Firebase Projects](actions/list-firebase-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-firebase-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Creates an access token for Firebase. |

### Android Sha Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Create Android SHA Certificate](actions/create-android-sha-certificate.md) | POST | Creates an Android SHA certificate in Firebase. |
| [Delete Android SHA Certificate](actions/delete-android-sha-certificate.md) | DELETE | Deletes an Android SHA certificate from Firebase. |
| [List Android SHA Certificates](actions/list-android-sha-certificates.md) | GET | Retrieves Android SHA certificates from Firebase. |

### Firebase Admin Sdk Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Admin SDK Config](actions/get-admin-sdk-config.md) | GET | Retrieves Admin SDK config for a Firebase project. |

### Firebase Analytics Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Details](actions/get-analytics-details.md) | GET | Retrieves Google Analytics details for a Firebase project. |

### Firebase Android App

| Action | Method | Description |
| --- | --- | --- |
| [Create Android App](actions/create-android-app.md) | POST | Creates an Android app in Firebase. |
| [Get Android App](actions/get-android-app.md) | GET | Retrieves an Android app from Firebase. |
| [List Android Apps](actions/list-android-apps.md) | GET | Retrieves Android apps from Firebase. |
| [Remove Android App](actions/remove-android-app.md) | DELETE | Removes an Android app from Firebase. |
| [Undelete Android App](actions/undelete-android-app.md) | PUT | Restores a removed Android app in Firebase. |
| [Update Android App](actions/update-android-app.md) | PUT | Updates an existing Android app in Firebase. |

### Firebase Android App Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Android App Config](actions/get-android-app-config.md) | GET | Retrieves Android app config from Firebase. |

### Firebase App

| Action | Method | Description |
| --- | --- | --- |
| [Search Project Apps](actions/search-project-apps.md) | GET | Finds apps in a Firebase project. |

### Firebase Ios App

| Action | Method | Description |
| --- | --- | --- |
| [Create iOS App](actions/create-ios-app.md) | POST | Creates an iOS app in Firebase. |
| [Get iOS App](actions/get-ios-app.md) | GET | Retrieves an iOS app from Firebase. |
| [List iOS Apps](actions/list-ios-apps.md) | GET | Retrieves iOS apps from Firebase. |
| [Remove iOS App](actions/remove-ios-app.md) | DELETE | Removes an iOS app from Firebase. |
| [Undelete iOS App](actions/undelete-ios-app.md) | PUT | Restores a removed iOS app in Firebase. |
| [Update iOS App](actions/update-ios-app.md) | PUT | Updates an existing iOS app in Firebase. |

### Firebase Ios App Config

| Action | Method | Description |
| --- | --- | --- |
| [Get iOS App Config](actions/get-ios-app-config.md) | GET | Retrieves iOS app config from Firebase. |

### Firebase Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Firebase To Project](actions/add-firebase-to-project.md) | POST | Adds Firebase to a Google Cloud project. |
| [Get Firebase Project](actions/get-firebase-project.md) | GET | Retrieves a Firebase project. |
| [List Firebase Projects](actions/list-firebase-projects.md) | GET | Retrieves Firebase projects. |
| [Update Firebase Project](actions/update-firebase-project.md) | PUT | Updates an existing Firebase project. |

### Firebase Project Analytics Link

| Action | Method | Description |
| --- | --- | --- |
| [Add Google Analytics To Project](actions/add-google-analytics-to-project.md) | POST | Adds Google Analytics to a Firebase project. |
| [Remove Analytics From Project](actions/remove-analytics-from-project.md) | DELETE | Removes Google Analytics from a Firebase project. |

### Firebase Web App

| Action | Method | Description |
| --- | --- | --- |
| [Create Web App](actions/create-web-app.md) | POST | Creates a web app in Firebase. |
| [Get Web App](actions/get-web-app.md) | GET | Retrieves a web app from Firebase. |
| [List Web Apps](actions/list-web-apps.md) | GET | Retrieves web apps from Firebase. |
| [Remove Web App](actions/remove-web-app.md) | DELETE | Removes a web app from Firebase. |
| [Undelete Web App](actions/undelete-web-app.md) | PUT | Restores a removed web app in Firebase. |
| [Update Web App](actions/update-web-app.md) | PUT | Updates an existing web app in Firebase. |

### Firebase Web App Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Web App Config](actions/get-web-app-config.md) | GET | Retrieves web app config from Firebase. |

### Google Cloud Project

| Action | Method | Description |
| --- | --- | --- |
| [List Available Projects](actions/list-available-projects.md) | GET | Retrieves available Google Cloud projects for Firebase. |

### Operation

| Action | Method | Description |
| --- | --- | --- |
| [Get Operation](actions/get-operation.md) | GET | Retrieves an operation from Firebase. |

