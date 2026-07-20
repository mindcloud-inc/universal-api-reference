# List Contract Files with Oneflow

Retrieves contract files from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts/:contractId/files`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [List Contract Files](https://developer.oneflow.com/reference/get-contract-files)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
