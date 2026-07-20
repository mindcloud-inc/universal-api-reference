# Get document publication with MoySklad

Retrieves the document publication from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/:id/publication`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get document publication](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-publikaciia-dokumentow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
