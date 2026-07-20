# Create Conversation with SparrowDesk

Creates a conversation in SparrowDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Create Conversation](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee` | body | `string` | no | Assignee email address. |
| `brand_id` | body | `number` | no | Optional SparrowDesk brand ID. |
| `description` | body | `string` | yes | Conversation description text. |
| `priority` | body | `string` | no | Priority: Low, Medium, High, or Urgent. |
| `requested_by` | body | `string` | yes | Requester email address or phone number. |
| `source` | body | `string` | no | Source: Mail or Call. |
| `status` | body | `string` | no | Status: Open, Pending, Resolved, or Closed. |
| `subject` | body | `string` | yes | Conversation subject. |
| `team_id` | body | `number` | no | Optional SparrowDesk team ID. |
