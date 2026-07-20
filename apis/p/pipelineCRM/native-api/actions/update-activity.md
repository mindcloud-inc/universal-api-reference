# Update Activity with Pipeline CRM

Updates an existing activity note in Pipeline CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notes/:id`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [Update Activity](https://app.pipelinecrm.com/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Activity ID |
| `note.title` | body | `string` | no | The note title, if any. |
| `note.content` | body | `string` | no | The note content. |
| `note.user_id` | body | `number` | no | The owner user ID of the note. |
| `note.deal_id` | body | `number` | no | The deal ID associated with the note. |
| `note.company_id` | body | `number` | no | The company ID associated with the note. |
| `note.person_id` | body | `number` | no | The person ID associated with the note. |
| `note.milestone_id` | body | `number` | no | The milestone ID associated with the note. |
| `note.note_category_id` | body | `number` | no | The category ID of the note. |
| `note.notify_user_ids[]` | body | `array<number>` | no | User IDs to notify when new comments are added. |
