# Run Field Action with QuintaDB

Runs a field action on a QuintaDB record.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/:action_property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Run Field Action](https://quintadb.com/api/index#action)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `action_property_id` | path | `string` | yes |
| `dtype_id` | query | `string` | yes |
