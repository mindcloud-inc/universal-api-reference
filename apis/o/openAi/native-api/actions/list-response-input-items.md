# List Response Input Items with Open AI

Retrieves input items from a response in Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/responses/:response_id/input_items`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [List Response Input Items](https://developers.openai.com/api/reference/resources/responses/subresources/input_items/methods/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | path | `string` | yes | The ID of the response whose input items are listed. |
| `limit` | query | `date` | no | Maximum number of input items to return. |
| `order` | query | `list` | no | Sort order for returned items. |
| `after` | query | `string` | no | Return items after this cursor. |
| `before` | query | `string` | no | Return items before this cursor. |
