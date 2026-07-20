# Get session with Appwrite

Retrieves session details from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/sessions/{sessionId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get session](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Session ID. Use the string 'current' to get the current device session. |
