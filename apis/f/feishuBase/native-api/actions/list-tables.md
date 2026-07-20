# List Tables with Feishu Base

Retrieves tables from a Feishu Base app.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_token/tables`
- **Base URL:** `https://open.feishu.cn/open-apis/bitable/v1`
- **Official documentation:** [List Tables](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_token` | path | `string` | yes | Unique identifier of the Feishu Base app. |
| `page_token` | query | `string` | no | Pagination token returned by the previous page. |
| `page_size` | query | `number` | no | Maximum number of tables to return. |
