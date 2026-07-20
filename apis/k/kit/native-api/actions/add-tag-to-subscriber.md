# Add Tag to Subscriber with Kit

Adds a tag to a Kit subscriber.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/:tag_id/subscribers/:id`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Add Tag to Subscriber](https://developers.kit.com/api-reference/tags/tag-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `number` | yes | Tag ID from the path parameter. |
| `id` | path | `number` | yes | Subscriber ID from the path parameter. |
