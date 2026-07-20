# List Podcast Distribution Channels with Simplecast

Retrieves distribution channels for a podcast from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/distribution_channels`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Podcast Distribution Channels](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
