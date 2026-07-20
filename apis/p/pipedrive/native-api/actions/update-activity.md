# Update Activity with Pipedrive

Updates an existing activity in Pipedrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2/activities/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Update Activity](https://developers.pipedrive.com/docs/api/v1/Activities#updateActivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `string` | no | Due date (YYYY-MM-DD). |
| `due_time` | body | `string` | no | Due time (HH:mm). |
| `duration` | body | `string` | no | Duration in HH:mm format. |
| `id` | path | `number` | yes | Unique ID of the activity to update. |
| `lead_id` | body | `string` | no | Linked lead ID. |
| `note` | body | `string` | no | Activity note. |
| `priority` | body | `string` | no | Activity priority. |
| `subject` | body | `string` | no | Activity subject. |
| `type` | body | `string` | no | Activity type. |
| `owner_id` | body | `number` | no | Owner user ID. |
| `deal_id` | body | `number` | no | Linked deal ID. |
| `person_id` | body | `number` | no | Linked person ID. |
| `org_id` | body | `number` | no | Linked organization ID. |
| `done` | body | `boolean` | no | Completion state. |
