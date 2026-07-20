# Update Table Rows with Rocketadmin

## Endpoint

- **Method:** `PUT`
- **Path:** `/table/rows/update/:connectionId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Update Table Rows](https://docs.rocketadmin.com/api-reference/table-controller-update-rows-in-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name for the target row set. |
