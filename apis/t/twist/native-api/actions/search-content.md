# Search Content with Twist

Finds threads and messages in Twist by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Search Content](https://developer.twist.com/v3/#search-for-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor_mark` | query | `string` | no | Token used for pagination. |
| `limit` | query | `number` | no | Limits the number of results returned. |
| `query` | query | `string` | yes | The full-text query to search for. |
| `title` | query | `string` | no | Filter by thread or conversation title. |
| `type` | query | `string` | no | Filter by object type: threads, messages, or all. |
| `workspace_id` | query | `number` | yes | The workspace to search. |
