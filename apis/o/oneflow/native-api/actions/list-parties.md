# List Parties with Oneflow

Retrieves contract parties from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts/:contractId/parties`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [List Parties](https://developer.oneflow.com/reference/get-parties)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
