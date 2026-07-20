# Add Comment with Kintone

Creates a comment on a Kintone record.

## Endpoint

- **Method:** `POST`
- **Path:** `/record/comment.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Add Comment](https://kintone.dev/en/docs/kintone/rest-api/records/add-comment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `record` | body | `number` | yes | The Kintone record ID to comment on. |
| `comment.text` | body | `string` | yes | The text body of the comment. |
| `comment.mentions` | body | `list<object>` | no | Optional mention objects to include with the comment. |
