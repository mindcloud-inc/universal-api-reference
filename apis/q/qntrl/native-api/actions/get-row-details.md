# Get Row Details with Qntrl

Retrieves row details from a Qntrl table.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/table/[:table_id]/row/[:row_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Row Details](https://core.qntrl.com/apidoc.html#getRow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `row_id` | path | `string` | no | Qntrl row ID. |
| `table_id` | path | `string` | no | Qntrl table ID. |
