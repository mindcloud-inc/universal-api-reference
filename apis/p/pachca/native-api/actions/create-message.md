# Create message with Pachca

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create message](https://dev.pachca.com/reference/messages-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `object` | yes | Message parameters object. |
| `message.entity_id` | body | `number` | yes | Target chat/thread entity ID. |
| `message.entity_type` | body | `string` | no | Entity type. Defaults to discussion. |
| `message.content` | body | `string` | yes | Message text. |
| `link_preview` | body | `boolean` | no | Whether to display a link preview. |
