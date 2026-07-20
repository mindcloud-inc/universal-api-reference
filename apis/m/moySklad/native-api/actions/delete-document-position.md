# Delete document position with MoySklad

Deletes a document position from MoySklad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `entity/:entityType/:id/positions/:positionId`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Delete document position](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
| `positionId` | path | `string` | yes | MoySklad position ID. |
