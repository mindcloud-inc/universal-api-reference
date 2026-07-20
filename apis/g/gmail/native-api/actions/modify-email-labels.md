# Modify Email Labels with Google Mail

Updates labels on a Gmail message.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:id/modify`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Modify Email Labels](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the message to modify. |
