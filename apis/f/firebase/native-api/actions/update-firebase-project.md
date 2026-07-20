# Update Firebase Project with Firebase

Updates an existing Firebase project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1beta1/projects/[:projectId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Update Firebase Project](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `updateMask` | query | `string` | no | Comma-separated FirebaseProject fields to update. |
| `displayName` | body | `string` | no | User-assigned Firebase project display name. |
| `etag` | body | `string` | no | Checksum used to avoid overwriting stale project data. |
