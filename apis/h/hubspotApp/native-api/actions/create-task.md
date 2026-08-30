# Create Task with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/tasks`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Task](https://developers.hubspot.com/docs/api-reference/latest/crm/activities/tasks/guide)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `properties` | body | `object` | yes |
| `properties.hs_timestamp` | body | `date` | yes |
| `properties.hs_task_subject` | body | `string` | no |
| `properties.hs_task_body` | body | `string` | no |
| `properties.hubspot_owner_id` | body | `string` | no |
| `properties.hs_task_status` | body | `string` | no |
| `properties.hs_task_priority` | body | `string` | no |
| `properties.hs_task_type` | body | `string` | no |
| `properties.hs_task_reminders` | body | `string` | no |
| `associations[]` | body | `array<object>` | no |
| `associations[].to` | body | `object` | no |
| `associations[].to.id` | body | `string` | no |
| `associations[].types[]` | body | `array<object>` | no |
| `associations[].types[].associationCategory` | body | `string` | no |
| `associations[].types[].associationTypeId` | body | `number` | no |
