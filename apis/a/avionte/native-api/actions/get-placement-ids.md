# Get Placement IDs with Avionte

Retrieves placement IDs from Avionte.

## Endpoint

- **Method:** `GET`
- **Path:** `front-office/v1/placements/ids/:page/:pageSize`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Get Placement IDs](https://developer.avionte.com/reference/placementids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | path | `number` | yes | The page number to request. |
| `pageSize` | path | `number` | yes | The number of results per page. |
