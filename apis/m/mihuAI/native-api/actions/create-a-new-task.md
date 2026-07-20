# Create a New Task with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Create a New Task](https://developers.mihu.ai/api-reference/tasks/create-a-new-task-call-or-whatsapp-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent_uuid` | body | `string` | yes |
| `auto_queue` | body | `boolean` | no |
| `campaign_uuid` | body | `string` | no |
| `contact_uuid` | body | `string` | no |
| `description` | body | `string` | no |
| `priority` | body | `number` | no |
| `scheduled_at` | body | `string` | yes |
| `timezone` | body | `string` | no |
| `title` | body | `string` | yes |
| `type` | body | `string` | yes |
