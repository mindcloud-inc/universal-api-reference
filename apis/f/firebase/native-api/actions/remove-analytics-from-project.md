# Remove Analytics From Project with Firebase

Removes Google Analytics from a Firebase project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]:removeAnalytics`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Remove Analytics From Project](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/removeAnalytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `analyticsPropertyId` | body | `string` | no | Google Analytics property ID associated with the Firebase project. |
