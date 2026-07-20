# Update Storage with Claid AI

Updates a storage connector in Claid AI by storage ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `storage/storages/:storage_id`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Update Storage](https://docs.claid.ai/storage-connectors/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Maximum length: 50. |
| `parameters` | body | `object` | no | — |
| `storage_id` | path | `number` | yes | — |
| `type` | body | `string` | no | Accepted values: `0`, `1`, `2`. |
