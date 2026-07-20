# Send Text Message To Contact with Fliqr AI

Sends a text message to a contact in Fliqr AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/send/text`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Send Text Message To Contact](https://docs.fliqr.ai/api-reference/users/post-users-sendtext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Fliqr contact user ID. |
| `text` | body | `string` | no | Text message content. |
| `channel` | body | `string` | no | Messaging channel. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
