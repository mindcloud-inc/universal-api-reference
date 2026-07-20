# Trash Email with Google Mail

Moves a Gmail message to trash.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:id/trash`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Trash Email](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/trash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gmail message ID to trash. |
