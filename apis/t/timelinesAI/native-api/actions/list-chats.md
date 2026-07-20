# List Chats with TimelinesAI

Retrieves chats from your TimelinesAI workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [List Chats](https://timelinesai.mintlify.app/public-api-reference/get-full-or-filtered-list-of-all-chats-in-the-workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | query | `string` | no | Filter chats by label. Use a comma-separated list to match any listed label. |
| `whatsapp_account_id` | query | `string` | no | Filter chats by one or more WhatsApp account IDs in wid format. |
| `group` | query | `boolean` | no | Filter for group chats or direct chats. |
| `responsible` | query | `string` | no | Filter chats assigned to specific users by email address. Use commas for multiple values. |
| `name` | query | `string` | no | Filter chats whose name contains one or more strings. Use commas for multiple values. |
| `phone` | query | `string` | no | Filter direct chats by a phone number. |
| `read` | query | `boolean` | no | Filter for read or unread chats. |
| `closed` | query | `boolean` | no | Filter for closed or open chats. |
| `chatgpt_autoresponse_enabled` | query | `boolean` | no | Filter chats where ChatGPT auto-response is enabled or disabled. |
| `page` | query | `number` | no | Page number starting at 1. |
| `created_after` | query | `date` | no | Filter chats created after this timestamp. |
| `created_before` | query | `date` | no | Filter chats created before this timestamp. |
