# List Sponsor Podcasts with Podscan

Retrieves podcasts for a sponsor from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/sponsors/{sponsor}/podcasts`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [List Sponsor Podcasts](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sponsor` | path | `string` | yes | The sponsor ID. |
