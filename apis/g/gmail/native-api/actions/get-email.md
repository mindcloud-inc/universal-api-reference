# Get Email with Google Mail

Retrieves a Gmail message.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Email](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The immutable ID of the message.. Use the List Emails action to find this value. |
