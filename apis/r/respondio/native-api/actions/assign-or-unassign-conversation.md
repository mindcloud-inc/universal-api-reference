# Assign Or Unassign Conversation with respond.io

Updates a conversation assignee in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:identifier/conversation/assignee`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Assign Or Unassign Conversation](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/conversation-api.yml/paths/~1contact~1%7Bidentifier%7D~1conversation~1assignee/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee` | body | `string` | yes | Assignee user identifier or null to unassign. |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
