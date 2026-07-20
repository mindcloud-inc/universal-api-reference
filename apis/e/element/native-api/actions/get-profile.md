# Get Profile with Element

Retrieves a user's profile from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/profile/:userId`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Profile](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3profileuserid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Matrix user ID, for example @alice:matrix.org. |
