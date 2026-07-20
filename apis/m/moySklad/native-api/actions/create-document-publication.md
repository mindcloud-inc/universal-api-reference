# Create document publication with MoySklad

Creates a document publication in MoySklad.

## Endpoint

- **Method:** `POST`
- **Path:** `entity/:entityType/:id/publication`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Create document publication](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-publikaciia-dokumentow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type. |
| `id` | path | `string` | yes | MoySklad document ID. |
