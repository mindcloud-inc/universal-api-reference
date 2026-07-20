# Search Records with QuintaDB

Finds records in QuintaDB by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/:app_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Search Records](https://quintadb.com/api/index#search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | body | `string` | yes |
| `limit` | body | `string` | no |
| `search` | body | `string` | yes |
| `view` | body | `string` | no |
