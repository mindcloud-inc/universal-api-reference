# Query Tasks with ProjectManager

Finds tasks in ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tasks`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Query Tasks](https://developer.projectmanager.com/api-reference/task/query-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | The number of records to return |
| `$skip` | query | `number` | no | Skips the given number of records and then returns $top records |
| `$filter` | query | `string` | no | Filter the expression according to oData queries |
| `$orderby` | query | `string` | no | Order collection by this field. |
| `$expand` | query | `string` | no | Include related data in the response |
