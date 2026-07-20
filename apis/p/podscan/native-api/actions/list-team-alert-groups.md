# List Team Alert Groups with Podscan

Retrieves alert groups for a team from Podscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/{team}/alert-groups`
- **Base URL:** `https://podscan.fm/api/v1`
- **Official documentation:** [List Team Alert Groups](https://podscan.fm/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | The team ID. |
