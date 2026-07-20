# List Connected Files with Tako

Retrieves connected files from Tako.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/beta/file_connector`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [List Connected Files](https://docs.tako.com/api-reference/file-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | query | `string` | no | Optional file ID to fetch one connected file instead of the full list. |
