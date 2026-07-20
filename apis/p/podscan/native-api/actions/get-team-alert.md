# Get Team Alert with Podscan

Retrieves a team alert from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/{team}/alerts/{alert}`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [Get Team Alert](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alert` | path | `string` | yes | The alert ID. |
| `team` | path | `string` | yes | The team ID. |
