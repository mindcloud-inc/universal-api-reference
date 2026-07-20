# Set Display Name with Element

Updates a user's display name in Element.

## Endpoint

- **Method:** `PUT`
- **Path:** `/_matrix/client/v3/profile/:userId/displayname`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Set Display Name](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3profileuseriddisplayname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Matrix user ID to update. |
| `displayname` | body | `string` | yes | New display name for the user profile. |
