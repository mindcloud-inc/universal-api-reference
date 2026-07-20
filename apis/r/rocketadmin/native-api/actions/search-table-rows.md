# Search Table Rows with Rocketadmin

## Endpoint

- **Method:** `POST`
- **Path:** `/table/rows/find/:connectionId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Search Table Rows](https://docs.rocketadmin.com/api-reference/table-controller-find-all-rows-with-body-filter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name within the selected connection. |
