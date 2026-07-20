# List document positions with MoySklad

Retrieves document positions from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/:id/positions`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List document positions](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
