# Add Comment with SmartSuite

Creates a new comment in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Add Comment](https://developers.smartsuite.com/docs/solution-data/comments/add-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `record` | query | `string` | yes | The SmartSuite record ID to add the comment to. |
| `application` | body | `string` | yes | The SmartSuite table ID that owns the record. |
| `messageHtml` | body | `string` | yes | The comment body as HTML, for example `<p>Hello</p>`. |
| `assigned_to` | body | `string` | no | Optional SmartSuite assignee member ID for the comment. |
| `parent_comment` | body | `string` | no | Optional parent comment ID when replying to an existing comment. |
