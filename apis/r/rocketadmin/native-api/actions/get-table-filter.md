# Get Table Filter with Rocketadmin

## Endpoint

- **Method:** `GET`
- **Path:** `/table-filters/:connectionId/:filterId`
- **Base URL:** `https://app.rocketadmin.com/api`
- **Official documentation:** [Get Table Filter](https://docs.rocketadmin.com/api-reference/table-filters-controller-find-table-filter-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Rocketadmin connection identifier from the path. |
| `filterId` | path | `string` | yes | Rocketadmin table filter identifier from the path. |
