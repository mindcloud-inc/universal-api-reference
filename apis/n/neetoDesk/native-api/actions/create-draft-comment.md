# Create Draft Comment with NeetoDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticket_id/drafts`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Create Draft Comment](https://apidocs.neetodesk.com/api-reference/comments/create-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Identifier of the ticket. |
| `content` | body | `string` | yes | Content for the draft comment. |
| `comment_type` | body | `string` | no | Type of draft comment. |
| `author_email` | body | `string` | no | Email of the person creating the draft. |
