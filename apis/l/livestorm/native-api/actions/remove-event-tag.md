# Remove Event Tag with Livestorm

Removes a tag from an event in Livestorm.

## Endpoint

- **Method:** `DELETE`
- **Path:** `events/:id/tags`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Remove Event Tag](https://developers.livestorm.co/reference/delete_events-id-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `data.attributes.title` | body | `string` | yes | Tag title to remove |
