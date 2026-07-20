# Run Field Actions with QuintaDB

Runs a field action on multiple QuintaDB records.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/:action_property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Run Field Actions](https://quintadb.com/api/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `action_property_id` | path | `string` | yes |
| `json_dtype_ids` | query | `string` | yes |
| `run_by_all_table_or_report` | query | `string` | no |
| `view` | query | `string` | no |
