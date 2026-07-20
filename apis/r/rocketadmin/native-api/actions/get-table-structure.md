# Get Table Structure with Rocketadmin

## Endpoint

- **Method:** `GET`
- **Path:** `/table/structure/:connectionId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Get Table Structure](https://docs.rocketadmin.com/api-reference/table-controller-get-table-structure)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name within the selected connection. |
