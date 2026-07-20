# List Records with Feishu Base

Retrieves records from a Feishu Base table.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_token/tables/:table_id/records`
- **Base URL:** `https://open.feishu.cn/open-apis/bitable/v1`
- **Official documentation:** [List Records](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table-record/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_token` | path | `string` | yes | Unique identifier of the Feishu Base app. |
| `table_id` | path | `string` | yes | Unique identifier of the table inside the Feishu Base app. |
| `view_id` | query | `string` | no | Optional view to scope the returned records. |
| `filter` | query | `string` | no | Optional Feishu record filter expression. |
| `sort` | query | `string` | no | Optional Feishu sort expression array encoded as JSON text. |
| `field_names` | query | `string` | no | Optional array of field names encoded as JSON text. |
| `text_field_as_array` | query | `boolean` | no | Return multiline text values as an array-rich structure when true. |
| `user_id_type` | query | `string` | no | Identity type to use for returned user references. |
| `display_formula_ref` | query | `boolean` | no | Return formula and lookup fields using the referenced field format when true. |
| `automatic_fields` | query | `boolean` | no | Include automatically computed fields such as created and modified metadata when true. |
| `page_token` | query | `string` | no | Pagination token returned by the previous page. |
| `page_size` | query | `number` | no | Maximum number of records to return. |
