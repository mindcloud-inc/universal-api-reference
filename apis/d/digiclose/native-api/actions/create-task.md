# Create Task with Digiclose

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://app.digiclose.ai/api/v1`
- **Official documentation:** [Create Task](https://app.digiclose.ai/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignee_id` | body | `number` | yes |
| `category_id` | body | `number` | yes |
| `contact_id` | body | `number` | yes |
| `creator_id` | body | `number` | yes |
| `description` | body | `string` | yes |
| `due_at` | body | `string` | yes |
