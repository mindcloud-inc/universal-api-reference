# Create Storage with Claid AI

Creates a storage connector in Claid AI.

## Endpoint

- **Method:** `POST`
- **Path:** `storage/storages`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Create Storage](https://docs.claid.ai/storage-connectors/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Maximum length: 50. |
| `parameters` | body | `object` | yes | — |
| `type` | body | `string` | yes | Accepted values: `0`, `1`, `2`. |
