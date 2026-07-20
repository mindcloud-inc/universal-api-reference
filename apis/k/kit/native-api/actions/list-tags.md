# List Tags with Kit

Lists tags in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Tags](https://developers.kit.com/api-reference/tags/list-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch next page using pagination end cursor. |
| `before` | query | `string` | no | Fetch previous page using pagination start cursor. |
| `include_total_count` | query | `boolean` | no | Include total record count in response when true. |
| `per_page` | query | `number` | no | Results per page (default 500, max 1000). |
