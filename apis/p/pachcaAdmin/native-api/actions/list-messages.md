# List Messages with Pachca (Admin)

Retrieves messages from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Messages](https://dev.pachca.com/api/messages/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | query | `number` | yes | — |
| `order` | query | `string` | no | Sort direction. |
| `sort` | query | `string` | no | Sort direction hint from provider docs. |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
