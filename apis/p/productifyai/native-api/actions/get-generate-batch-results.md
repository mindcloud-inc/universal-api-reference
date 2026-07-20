# Get Generate Batch Results with Productify.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/Result/Generate`
- **Base URL:** `https://api.productify.ai`
- **Official documentation:** [Get Generate Batch Results](https://api.productify.ai/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | body | `number` | yes | Batch identifier to retrieve results for. |
| `pageNumber` | body | `number` | no | — |
| `pageSize` | body | `number` | no | — |
