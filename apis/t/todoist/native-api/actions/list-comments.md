# List Comments with Todoist

Retrieves comments from Todoist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/comments`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [List Comments](https://developer.todoist.com/api/v1/#tag/Comments/operation/get_comments_api_v1_comments_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Project ID to list comments from. Use either Project ID or Task ID. |
| `task_id` | query | `string` | no | Task ID to list comments from. Use either Task ID or Project ID. |
| `cursor` | query | `string` | no | Cursor for the next page of results. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `public_key` | query | `string` | no | Public key used for shared-resource access where applicable. |
