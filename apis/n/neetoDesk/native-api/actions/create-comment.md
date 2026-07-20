# Create Comment with NeetoDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticket_id/comments`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Create Comment](https://apidocs.neetodesk.com/api-reference/comments/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Identifier of the ticket. |
| `author_email` | body | `string` | yes | Email address of the comment author. |
| `content` | body | `string` | yes | Content of the comment. |
| `comment_type` | body | `string` | no | Type of comment. |
