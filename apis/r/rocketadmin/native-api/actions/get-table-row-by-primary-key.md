# Get Table Row By Primary Key with Rocketadmin

## Endpoint

- **Method:** `GET`
- **Path:** `/table/row/:connectionId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Get Table Row By Primary Key](https://docs.rocketadmin.com/api-reference/table-controller-get-row-by-primary-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name for the target row. |
