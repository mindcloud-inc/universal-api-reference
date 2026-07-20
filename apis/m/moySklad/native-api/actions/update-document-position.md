# Update document position with MoySklad

Updates a document position in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/:entityType/:id/positions/:positionId`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update document position](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
| `positionId` | path | `string` | yes | MoySklad position ID. |
| `quantity` | body | `number` | yes | MoySklad quantity argument. |
