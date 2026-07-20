# Add Google Analytics To Project with Firebase

Adds Google Analytics to a Firebase project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]:addGoogleAnalytics`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Add Google Analytics To Project](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/addGoogleAnalytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `analyticsAccountId` | body | `string` | no | Existing Google Analytics account ID to link. |
| `analyticsPropertyId` | body | `string` | no | Existing Google Analytics property ID to associate with the Firebase project. |
