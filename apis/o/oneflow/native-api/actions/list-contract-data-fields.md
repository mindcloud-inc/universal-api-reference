# List Contract Data Fields with Oneflow

Retrieves contract data fields from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts/:contractId/data_fields`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [List Contract Data Fields](https://developer.oneflow.com/reference/get-contract-data-fields)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
