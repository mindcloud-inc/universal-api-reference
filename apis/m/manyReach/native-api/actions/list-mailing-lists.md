# List Mailing Lists with ManyReach

Retrieves mailing lists from ManyReach.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.manyreach.com/api/v2/lists`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [List Mailing Lists](https://api.manyreach.com/api#v2/tag/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number (1-indexed). |
| `limit` | query | `number` | no | Items per page. Default 100, max 1000. |
| `startingAfter` | query | `number` | no | Cursor for the next page. |
