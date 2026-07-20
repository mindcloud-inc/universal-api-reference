# List Datasets for Owner with data.world

Retrieves datasets for an owner from data.world.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasets/{owner}`
- **Base URL:** `https://api.data.world/v0`
- **Official documentation:** [List Datasets for Owner](https://developer.data.world/reference/getdatasetsbyowner-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | User or organization owner of the dataset. |
