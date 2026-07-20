# List Broadcasts with Kit

Lists broadcasts in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/broadcasts`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Broadcasts](https://developers.kit.com/api-reference/broadcasts/list-broadcasts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Number of results per page (default 500, max 1000). |
| `after` | query | `string` | no | Fetch next page using end_cursor. |
| `before` | query | `string` | no | Fetch previous page using start_cursor. |
| `include_total_count` | query | `boolean` | no | Include total count in response. |
