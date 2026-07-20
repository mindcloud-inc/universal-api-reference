# List Media Files with EZ Texting

Retrieves media files from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/media-files`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Media Files](https://developers.eztexting.com/reference/list_5-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[type][eq]` | query | `string` | no | Filter media files by type |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
