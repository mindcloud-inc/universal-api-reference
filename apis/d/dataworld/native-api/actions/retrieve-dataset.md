# Retrieve Dataset with data.world

Retrieves a dataset from data.world.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasets/{owner}/{id}`
- **Base URL:** `https://api.data.world/v0`
- **Official documentation:** [Retrieve Dataset](https://developer.data.world/reference/getdataset-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | User or organization owner of the dataset. |
| `id` | path | `string` | yes | Dataset identifier. |
