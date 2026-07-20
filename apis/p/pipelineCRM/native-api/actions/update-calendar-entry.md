# Update Calendar Entry with Pipeline CRM

Updates an existing calendar entry in Pipeline CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendar_entries/:id`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [Update Calendar Entry](https://app.pipelinecrm.com/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliver_reassignment_email` | query | `boolean` | no | Send an assignment email when the calendar entry owner changes. |
| `id` | path | `number` | yes | Calendar entry ID |
| `calendar_entry.type` | body | `string` | no | Calendar entry type: CalendarEvent or CalendarTask. |
| `calendar_entry.category_id` | body | `number` | no | The event category ID. |
| `calendar_entry.name` | body | `string` | no | The name of the task or event. |
| `calendar_entry.description` | body | `string` | no | A detailed description of the event. |
| `calendar_entry.start_time` | body | `string` | no | Start time for CalendarEvent entries. |
| `calendar_entry.end_time` | body | `string` | no | End time for CalendarEvent entries. |
| `calendar_entry.all_day` | body | `boolean` | no | Whether the event is all day. |
| `calendar_entry.due_date` | body | `date` | no | Due date for CalendarTask entries. |
| `calendar_entry.complete` | body | `boolean` | no | Whether the entry is complete. |
| `calendar_entry.association_id` | body | `number` | no | The associated person, company, or deal ID. |
| `calendar_entry.association_type` | body | `string` | no | Association type: Deal, Company, or Person. |
| `calendar_entry.company_id` | body | `number` | no | If directly tied to a company, the company ID. |
| `calendar_entry.calendar_entry_priority_id` | body | `number` | no | The event priority ID. |
