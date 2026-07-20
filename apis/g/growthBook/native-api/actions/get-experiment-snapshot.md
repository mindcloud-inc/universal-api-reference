# Get an experiment snapshot status with GrowthBook

Retrieves experiment snapshot status from GrowthBook.

## Endpoint

- **Method:** `GET`
- **Path:** `/snapshots/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get an experiment snapshot status](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource (a snapshot ID, not experiment ID) |
