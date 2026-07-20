# Update Tag with Magileads

Updates an existing tag in Magileads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:tag_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update Tag](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The updated tag color in hex. |
| `name` | body | `string` | no | The updated tag name. |
| `tag_id` | path | `number` | yes | The tag ID. |
