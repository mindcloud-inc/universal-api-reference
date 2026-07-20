# Untrash Email with Google Mail

Removes a Gmail message from trash.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:id/untrash`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Untrash Email](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/untrash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gmail message ID to restore from trash. |
