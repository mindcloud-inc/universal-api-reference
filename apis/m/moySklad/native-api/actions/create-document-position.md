# Create document position with MoySklad

Creates a document position in MoySklad.

## Endpoint

- **Method:** `POST`
- **Path:** `entity/:entityType/:id/positions`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Create document position](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
| `quantity` | body | `number` | yes | MoySklad quantity argument. |
