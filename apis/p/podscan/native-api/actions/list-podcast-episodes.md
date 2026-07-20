# List Podcast Episodes with Podscan

Retrieves episodes for a podcast from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/{podcast}/episodes`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [List Podcast Episodes](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast` | path | `string` | yes | The podcast ID. |
