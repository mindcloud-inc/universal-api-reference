# List Records with Gridly

Finds records in a specific Gridly view.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/:viewId/records`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Records](https://www.gridly.com/docs/api/#list-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view whose records you want to list. |
| `columnIds` | query | `string` | no | A comma-separated list of column IDs to include in the response. |
| `fetchFileOption` | query | `string` | no | How file cells should be represented. Supported values include `id`, `name`, and `all`. |
| `page` | query | `object` | no | Gridly paging object with `offset` and `limit`. |
| `query` | query | `object` | no | Gridly filter object keyed by column ID and operator. |
| `sort` | query | `object` | no | Gridly sort object keyed by column ID and direction. |
