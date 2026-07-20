# List Transcriptions with HappyScribe

Retrieves transcriptions from HappyScribe.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcriptions`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [List Transcriptions](https://dev.happyscribe.com/sections/product/#transcriptions-list-all-transcriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `string` | no | Optional folder ID to scope the list to a folder and its subfolders. |
| `organization_id` | query | `string` | yes | Workspace organization ID required by HappyScribe for listing transcriptions. |
| `page` | query | `number` | no | Optional page number. |
| `tags` | query | `string` | no | Optional list of tags to filter by. |
