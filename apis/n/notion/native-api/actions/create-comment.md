# Create Comment with Notion

Creates a new comment in Notion.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Create Comment](https://developers.notion.com/reference/create-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | body | `object` | no | Parent page or block object for a new comment thread. |
| `discussion_id` | body | `string` | no | Existing discussion ID for a reply comment. |
| `rich_text` | body | `list<object>` | yes | Comment content in Notion rich_text format. |
| `attachments` | body | `list<object>` | no | Optional attachments for the comment. |
