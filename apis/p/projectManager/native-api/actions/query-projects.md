# Query Projects with ProjectManager

Finds projects in ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/projects`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Query Projects](https://developer.projectmanager.com/api-reference/project/query-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | The number of records to return |
| `$skip` | query | `number` | no | Skips the given number of records and then returns $top records |
| `$filter` | query | `string` | no | Filter the expression according to oData queries |
| `$orderby` | query | `string` | no | Order collection by this field. |
| `$expand` | query | `string` | no | Include related data in the response |
