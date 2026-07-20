# Create Inbox with Agent Mail

Creates a new inbox in AgentMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Create Inbox](https://docs.agentmail.to/api-reference/inboxes/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | Client-provided idempotency ID. |
| `display_name` | body | `string` | no | Display name for the new inbox. |
| `domain` | body | `string` | no | Domain for the new inbox. |
| `username` | body | `string` | no | Username for the new inbox. |
