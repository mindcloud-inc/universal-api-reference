# Retrieve Project with data.world

Retrieves a data project from data.world.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{owner}/{id}`
- **Base URL:** `https://api.data.world/v0`
- **Official documentation:** [Retrieve Project](https://developer.data.world/reference/getproject-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | User or organization owner of the project. |
| `id` | path | `string` | yes | Project identifier. |
