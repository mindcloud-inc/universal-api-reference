# List Episode Entities with Podscan

Retrieves entities mentioned in an episode from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/{episodeId}/entities`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [List Episode Entities](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episodeId` | path | `string` | yes | The episode ID. |
