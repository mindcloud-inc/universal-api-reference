# List Users with Notion

Retrieves users from the connected Notion workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [List Users](https://developers.notion.com/reference/get-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | Number of users to return (max 100). |
| `start_cursor` | query | `string` | no | Pagination cursor returned by previous response. |
