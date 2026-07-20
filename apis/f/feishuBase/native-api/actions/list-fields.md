# List Fields with Feishu Base

Retrieves fields from a Feishu Base table.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_token/tables/:table_id/fields`
- **Base URL:** `https://open.feishu.cn/open-apis/bitable/v1`
- **Official documentation:** [List Fields](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table-field/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_token` | path | `string` | yes | Unique identifier of the Feishu Base app. |
| `table_id` | path | `string` | yes | Unique identifier of the table inside the Feishu Base app. |
| `view_id` | query | `string` | no | Optional view to scope the returned fields. |
| `text_field_as_array` | query | `boolean` | no | Return field descriptions as an array-rich structure when true. |
| `page_token` | query | `string` | no | Pagination token returned by the previous page. |
| `page_size` | query | `number` | no | Maximum number of fields to return. |
