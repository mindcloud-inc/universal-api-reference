# List Related Podcasts with Podscan

Retrieves related podcast recommendations from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/podcasts/{podcast}/related_podcasts`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [List Related Podcasts](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `podcast` | path | `string` | yes | The podcast ID. |
