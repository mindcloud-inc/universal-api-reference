# Retrieve Data Source Template with Notion

Retrieves a data source template page from Notion.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:template_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve Data Source Template](https://developers.notion.com/reference/retrieve-a-page)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2022-06-28` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | ID of the template. |
