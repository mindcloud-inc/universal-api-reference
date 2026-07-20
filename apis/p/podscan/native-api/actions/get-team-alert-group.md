# Get Team Alert Group with Podscan

Retrieves a team alert group from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/{team}/alert-groups/{group}`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [Get Team Alert Group](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | The alert group ID. |
| `team` | path | `string` | yes | The team ID. |
