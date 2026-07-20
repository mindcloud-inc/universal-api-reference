# Invite Channel Members with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/users/:userId/channels/:channelId/members`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Invite Channel Members](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/inviteChannelMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user who is the member of the channel. |
| `channelId` | path | `string` | yes | The channel's unique identifier. |
