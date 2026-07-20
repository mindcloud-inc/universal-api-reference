# Delete session with Appwrite

Deletes the session from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/account/sessions/{sessionId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete session](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Session ID. Use the string 'current' to delete the current device session. |
