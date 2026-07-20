# Search Recordings with Basecamp

Finds recordings in Basecamp by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/search.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Search Recordings](https://github.com/basecamp/bc3-api/blob/master/sections/search.md#search-recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID. |
| `q` | query | `string` | yes | Search query string. |
| `type` | query | `string` | no | Filter by recording type. |
| `bucket_id` | query | `number` | no | Filter by project ID. |
| `creator_id` | query | `number` | no | Filter by creator person ID. |
| `file_type` | query | `string` | no | Filter attachments by file type. |
| `exclude_chat` | query | `string` | no | Exclude chat results when set. |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of results per page. |
