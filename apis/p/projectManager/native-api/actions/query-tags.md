# Query Tags with ProjectManager

Finds tags in ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tags`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Query Tags](https://developer.projectmanager.com/api-reference/tag/query-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | The number of records to return |
| `$skip` | query | `number` | no | Skips the given number of records and then returns $top records |
| `$filter` | query | `string` | no | Filter the expression according to oData queries |
| `$orderby` | query | `string` | no | Order collection by this field. |
| `$expand` | query | `string` | no | Include related data in the response |
