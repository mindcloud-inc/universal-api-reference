# Get Department IDs with Avionte

Retrieves department IDs from Avionte.

## Endpoint

- **Method:** `GET`
- **Path:** `front-office/v1/departments/ids/:page/:pageSize`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Get Department IDs](https://developer.avionte.com/reference/get-department-ids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | path | `number` | yes | The page number to request. |
| `pageSize` | path | `number` | yes | The number of results per page. |
