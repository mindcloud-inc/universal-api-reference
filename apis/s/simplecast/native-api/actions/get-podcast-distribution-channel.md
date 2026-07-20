# Get Podcast Distribution Channel with Simplecast

Retrieves a podcast distribution channel from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/:podcast_id/distribution_channels/:distribution_channel_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Podcast Distribution Channel](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `distribution_channel_id` | path | `string` | yes | Simplecast distribution channel identifier. |
| `podcast_id` | path | `string` | yes | Simplecast podcast identifier. |
