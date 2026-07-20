# Discover Similar Podcasts with Podscan

Retrieves similar podcast recommendations from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/{podcast}/discover`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [Discover Similar Podcasts](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast` | path | `string` | yes | The podcast ID. |
