# Get Podcast Category with Simplecast

Retrieves a podcast category from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/categories/:category_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Podcast Category](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `string` | yes | Simplecast category identifier. |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
