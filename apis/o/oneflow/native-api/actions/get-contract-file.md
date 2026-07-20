# Get Contract File with Oneflow

Retrieves contract file details from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts/:contractId/files/:fileId`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Get Contract File](https://developer.oneflow.com/reference/get-a-contract-file-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
| `fileId` | path | `string` | yes | The Oneflow contract file ID. |
