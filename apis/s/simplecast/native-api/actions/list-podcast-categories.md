# List Podcast Categories with Simplecast

Retrieves categories for a podcast from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/categories`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Categories](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
