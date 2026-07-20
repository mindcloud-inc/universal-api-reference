# Get Contract Create Data with Oneflow

Retrieves contract creation data from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/helpers/contract_create_data`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Get Contract Create Data](https://developer.oneflow.com/reference/get-data-to-create-a-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extension_type` | query | `string` | no | Filter contract creation data by integration extension type. |
| `template_type_id` | query | `number` | no | Filter contract creation data by template type ID. |
