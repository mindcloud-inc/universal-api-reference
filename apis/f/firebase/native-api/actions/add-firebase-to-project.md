# Add Firebase To Project with Firebase

Adds Firebase to a Google Cloud project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]:addFirebase`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Add Firebase To Project](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/addFirebase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase or Google Cloud project ID. |
| `locationId` | body | `string` | no | Deprecated location ID from AddFirebaseRequest; may be ignored for newer projects. |
