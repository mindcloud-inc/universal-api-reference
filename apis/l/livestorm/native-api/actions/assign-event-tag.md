# Assign Event Tag with Livestorm

Assigns a tag to an event in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `events/:id/tags`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Assign Event Tag](https://developers.livestorm.co/reference/post_events-id-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `data.attributes.title` | body | `string` | yes | Tag title |
