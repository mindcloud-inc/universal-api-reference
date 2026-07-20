# List Table Filters with Rocketadmin

## Endpoint

- **Method:** `GET`
- **Path:** `/table-filters/:connectionId/all`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [List Table Filters](https://docs.rocketadmin.com/api-reference/table-filters-controller-find-table-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `tableName` | query | `string` | yes | Rocketadmin table name for the saved filter set. |
