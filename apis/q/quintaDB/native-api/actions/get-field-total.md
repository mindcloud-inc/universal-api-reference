# Get Field Total with QuintaDB

Retrieves a total for a QuintaDB field.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/sum/:entity_id/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Get Field Total](https://quintadb.com/api/index#get_total_by_column)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |
| `view` | query | `string` | no |
