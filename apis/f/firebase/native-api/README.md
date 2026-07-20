# Firebase: Native API Reference

A consolidated summary of Firebase's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://firebase.google.com/docs/reference/firebase-management/rest
- **OpenAPI specification:** https://firebase.googleapis.com/$discovery/rest?version=v1beta1
- **API base URL:** `https://firebase.googleapis.com`

## Authentication

### Service Account JWT

Use a Google service account to sign a JWT assertion and exchange it for an OAuth2 access token.

### Credentials

- **Client Email:** `clientEmail` · required · Service account client email used as the JWT issuer.
- **Private Key ID:** `privateKeyId` · required · Service account private key ID used as the JWT key identifier.
- **Private Key:** `privateKeySecret` · required · Service account RSA private key used to sign JWT assertions.
- **OAuth Scopes:** `scopes` · required · Space-separated Google OAuth scopes requested in the JWT assertion.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/service-account)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; minimum 1). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Firebase To Project](actions/add-firebase-to-project.md) | `POST /v1beta1/projects/[:projectId]:addFirebase` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/addFirebase) |
| [Add Google Analytics To Project](actions/add-google-analytics-to-project.md) | `POST /v1beta1/projects/[:projectId]:addGoogleAnalytics` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/addGoogleAnalytics) |
| [Create Android App](actions/create-android-app.md) | `POST /v1beta1/projects/[:projectId]/androidApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/create) |
| [Create Android SHA Certificate](actions/create-android-sha-certificate.md) | `POST /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/create) |
| [Create iOS App](actions/create-ios-app.md) | `POST /v1beta1/projects/[:projectId]/iosApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/create) |
| [Create Web App](actions/create-web-app.md) | `POST /v1beta1/projects/[:projectId]/webApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/create) |
| [Delete Android SHA Certificate](actions/delete-android-sha-certificate.md) | `DELETE /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha/[:shaHash]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/delete) |
| [Get Access Token](actions/get-access-token.md) | `POST https://oauth2.googleapis.com/token` | [docs](https://developers.google.com/identity/protocols/oauth2/service-account#httprest) |
| [Get Admin SDK Config](actions/get-admin-sdk-config.md) | `GET /v1beta1/projects/[:projectId]/adminSdkConfig` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/getAdminSdkConfig) |
| [Get Analytics Details](actions/get-analytics-details.md) | `GET /v1beta1/projects/[:projectId]/analyticsDetails` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/getAnalyticsDetails) |
| [Get Android App](actions/get-android-app.md) | `GET /v1beta1/projects/[:projectId]/androidApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/get) |
| [Get Android App Config](actions/get-android-app-config.md) | `GET /v1beta1/projects/[:projectId]/androidApps/[:appId]/config` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/getConfig) |
| [Get Firebase Project](actions/get-firebase-project.md) | `GET /v1beta1/projects/[:projectId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/get) |
| [Get iOS App](actions/get-ios-app.md) | `GET /v1beta1/projects/[:projectId]/iosApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/get) |
| [Get iOS App Config](actions/get-ios-app-config.md) | `GET /v1beta1/projects/[:projectId]/iosApps/[:appId]/config` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/getConfig) |
| [Get Operation](actions/get-operation.md) | `GET /v1beta1/operations/[:operationId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/operations/get) |
| [Get Web App](actions/get-web-app.md) | `GET /v1beta1/projects/[:projectId]/webApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/get) |
| [Get Web App Config](actions/get-web-app-config.md) | `GET /v1beta1/projects/[:projectId]/webApps/[:appId]/config` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/getConfig) |
| [List Android Apps](actions/list-android-apps.md) | `GET /v1beta1/projects/[:projectId]/androidApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/list) |
| [List Android SHA Certificates](actions/list-android-sha-certificates.md) | `GET /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/list) |
| [List Available Projects](actions/list-available-projects.md) | `GET /v1beta1/availableProjects` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/availableProjects/list) |
| [List Firebase Projects](actions/list-firebase-projects.md) | `GET /v1beta1/projects` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/list) |
| [List iOS Apps](actions/list-ios-apps.md) | `GET /v1beta1/projects/[:projectId]/iosApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/list) |
| [List Web Apps](actions/list-web-apps.md) | `GET /v1beta1/projects/[:projectId]/webApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/list) |
| [Remove Analytics From Project](actions/remove-analytics-from-project.md) | `POST /v1beta1/projects/[:projectId]:removeAnalytics` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/removeAnalytics) |
| [Remove Android App](actions/remove-android-app.md) | `POST /v1beta1/projects/[:projectId]/androidApps/[:appId]:remove` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/remove) |
| [Remove iOS App](actions/remove-ios-app.md) | `POST /v1beta1/projects/[:projectId]/iosApps/[:appId]:remove` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/remove) |
| [Remove Web App](actions/remove-web-app.md) | `POST /v1beta1/projects/[:projectId]/webApps/[:appId]:remove` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/remove) |
| [Search Project Apps](actions/search-project-apps.md) | `GET /v1beta1/projects/[:projectId]:searchApps` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/searchApps) |
| [Undelete Android App](actions/undelete-android-app.md) | `POST /v1beta1/projects/[:projectId]/androidApps/[:appId]:undelete` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/undelete) |
| [Undelete iOS App](actions/undelete-ios-app.md) | `POST /v1beta1/projects/[:projectId]/iosApps/[:appId]:undelete` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/undelete) |
| [Undelete Web App](actions/undelete-web-app.md) | `POST /v1beta1/projects/[:projectId]/webApps/[:appId]:undelete` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/undelete) |
| [Update Android App](actions/update-android-app.md) | `PATCH /v1beta1/projects/[:projectId]/androidApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/patch) |
| [Update Firebase Project](actions/update-firebase-project.md) | `PATCH /v1beta1/projects/[:projectId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/patch) |
| [Update iOS App](actions/update-ios-app.md) | `PATCH /v1beta1/projects/[:projectId]/iosApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/patch) |
| [Update Web App](actions/update-web-app.md) | `PATCH /v1beta1/projects/[:projectId]/webApps/[:appId]` | [docs](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/patch) |
