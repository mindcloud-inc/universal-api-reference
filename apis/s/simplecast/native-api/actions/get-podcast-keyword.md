# Get Podcast Keyword with Simplecast

Retrieves a podcast keyword from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/keywords/:keyword_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Podcast Keyword](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword_id` | path | `string` | yes | Simplecast keyword identifier. |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
