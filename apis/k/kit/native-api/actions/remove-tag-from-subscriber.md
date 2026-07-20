# Remove Tag From Subscriber with Kit

Removes a tag from a Kit subscriber.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tags/:tag_id/subscribers/:id`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Remove Tag From Subscriber](https://developers.kit.com/api-reference/tags/remove-tag-from-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `number` | yes | Tag ID from the path parameter. |
| `id` | path | `number` | yes | Subscriber ID from the path parameter. |
