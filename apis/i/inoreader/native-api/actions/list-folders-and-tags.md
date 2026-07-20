# List Folders and Tags with Inoreader

Retrieves folders and tags from Inoreader.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag/list`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [List Folders and Tags](https://www.inoreader.com/developers/tag-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `types` | query | `number` | no | Set to 1 to include the tag item type in the response. |
| `counts` | query | `number` | no | Set to 1 to include unread and unseen counts for tags and active searches. |
