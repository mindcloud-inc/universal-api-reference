# Update session with Appwrite

Updates the session in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/sessions/{sessionId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update session](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Session ID. Use the string 'current' to update the current device session. |
