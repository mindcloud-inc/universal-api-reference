# Update message with Pachca

## Endpoint

- **Method:** `PUT`
- **Path:** `/messages/{id}`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update message](https://dev.pachca.com/reference/messages-id-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Pachca message ID. |
| `message` | body | `object` | yes | Message parameters object. |
| `message.content` | body | `string` | no | Message text. |
