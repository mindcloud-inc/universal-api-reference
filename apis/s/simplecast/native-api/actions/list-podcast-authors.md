# List Podcast Authors with Simplecast

Retrieves authors for a podcast from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/authors`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Authors](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
