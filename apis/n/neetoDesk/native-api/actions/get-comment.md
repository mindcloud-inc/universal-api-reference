# Get Comment with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticket_id/comments/:comment_id`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Get Comment](https://apidocs.neetodesk.com/api-reference/comments/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Identifier of the ticket. |
| `comment_id` | path | `string` | yes | Identifier of the comment. |
