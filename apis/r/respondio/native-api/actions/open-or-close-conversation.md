# Open Or Close Conversation with respond.io

Updates a conversation status in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:identifier/conversation/status`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Open Or Close Conversation](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/conversation-api.yml/paths/~1contact~1%7Bidentifier%7D~1conversation~1status/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Closing category when closing conversation. |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
| `status` | body | `string` | yes | Conversation status value. |
| `summary` | body | `string` | no | Closing summary when closing conversation. |
