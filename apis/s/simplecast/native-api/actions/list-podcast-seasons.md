# List Podcast Seasons with Simplecast

Retrieves seasons for a podcast from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/seasons`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Seasons](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
