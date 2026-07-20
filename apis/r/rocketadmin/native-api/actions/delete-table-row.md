# Delete Table Row with Rocketadmin

## Endpoint

- **Method:** `DELETE`
- **Path:** `/table/row/:connectionId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Delete Table Row](https://docs.rocketadmin.com/api-reference/table-controller-delete-row-in-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name for the target row. |
