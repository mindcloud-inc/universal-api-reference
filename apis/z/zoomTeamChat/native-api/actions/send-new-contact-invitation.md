# Send New Contact Invitation with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/users/:userId/invitations`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Send New Contact Invitation](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/sendNewContactInvitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user who is the inviter. |
