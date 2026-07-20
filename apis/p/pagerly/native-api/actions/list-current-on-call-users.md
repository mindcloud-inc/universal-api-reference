# List Current On-Call Users with Pagerly

Retrieves current on-call users from Pagerly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/currentusers`
- **Base URL:** `https://api.pagerly.io/pagerly`
- **Official documentation:** [List Current On-Call Users](https://docs.pagerly.io/api/rotations-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamname` | query | `string` | yes | Exact Pagerly team name to query for current on-call users. |
