# List Key Comments with Lokalise

Retrieves comments for a Lokalise key.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/keys/:key_id/comments`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [List Key Comments](https://developers.lokalise.com/reference/list-key-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Lokalise project identifier. |
| `key_id` | path | `string` | yes | Lokalise key identifier. |
