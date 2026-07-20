# Add Activity with Pipedrive

Creates a new activity in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/activities`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Activity](https://developers.pipedrive.com/docs/api/v1/Activities#addActivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `string` | no | Due date (YYYY-MM-DD). |
| `due_time` | body | `string` | no | Due time (HH:mm). |
| `duration` | body | `string` | no | Duration in HH:mm format. |
| `lead_id` | body | `string` | no | Linked lead ID. |
| `note` | body | `string` | no | Activity note. |
| `priority` | body | `string` | no | Activity priority. |
| `subject` | body | `string` | yes | Activity subject. |
| `type` | body | `string` | yes | Activity type. |
| `owner_id` | body | `number` | no | Owner user ID. |
| `deal_id` | body | `number` | no | Linked deal ID. |
| `person_id` | body | `number` | no | Linked person ID. |
| `org_id` | body | `number` | no | Linked organization ID. |
| `done` | body | `boolean` | no | Completion state. |
