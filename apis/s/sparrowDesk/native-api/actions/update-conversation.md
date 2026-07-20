# Update Conversation with SparrowDesk

Updates an existing conversation in SparrowDesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/{{id}}`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Update Conversation](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee` | body | `string` | no | Updated assignee email address. |
| `id` | path | `number` | yes | SparrowDesk conversation ID. |
| `priority` | body | `string` | no | Updated priority value. |
| `source` | body | `string` | no | Updated source value. |
| `status` | body | `string` | no | Updated status value. |
| `subject` | body | `string` | no | Updated conversation subject. |
| `team_id` | body | `string` | no | Updated team assignment. |
