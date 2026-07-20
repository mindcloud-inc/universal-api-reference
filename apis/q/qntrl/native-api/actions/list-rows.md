# List Rows with Qntrl

Retrieves rows from a Qntrl table.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/table/[:table_id]/row`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Rows](https://core.qntrl.com/apidoc.html#getRows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `table_id` | path | `string` | no | Qntrl table ID. |
