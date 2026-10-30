# Create Dispatch with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/dispatches`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Dispatch](https://api.gocanvas.com/api/v3/docs#create-an-immediate-dispatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | body | `number` | yes | The identifier of the form. |
| `dispatch_type` | body | `list` | yes | Choose an immediate, scheduled, or recurring dispatch. Accepted values: `immediate_dispatch`, `recurring_dispatch`, `scheduled_dispatch`. |
| `assignee_id` | body | `number` | no | User assigned to the dispatch; omit to leave it unassigned. |
| `name` | body | `string` | no | Short name displayed on the Dispatch Calendar and calendar invitation. |
| `description` | body | `string` | no | Short description displayed on the assignee's mobile device. |
| `department_id` | body | `number` | no | Department for the dispatch; if omitted, GoCanvas uses the assignee's default department or the form's originating department. |
| `customer_id` | body | `number` | no | Customer to associate with the dispatch. |
| `project_id` | body | `number` | no | Project to associate with the dispatch. |
| `site_id` | body | `number` | no | Site to associate with the dispatch. |
| `responses[]` | body | `array<object>` | no | Form entry responses used to pre-populate the submission. |
| `responses[].entry_id` | body | `number` | no | Identifier of the form entry; entry GUID is an alternative in the immediate-dispatch documentation. |
| `responses[].entry_guid` | body | `string` | no | Entry GUID, an alternative to entry ID documented for immediate dispatches. |
| `responses[].value` | body | `string` | no | Response data for the entry. |
| `responses[].multi_key` | body | `string` | no | Looped value reference; required for looped forms. |
| `scheduled_at` | body | `string` | no | Required for scheduled and recurring dispatches; example: 12/1/2024 8:00:00 AM. |
| `scheduled_end` | body | `string` | no | Required for scheduled and recurring dispatches; example: 12/1/2024 12:00:00 PM. |
| `reminder_interval` | body | `number` | no | Minutes before the dispatch event to send a reminder. Scheduled-dispatch documentation lists this as optional and also as required. |
| `send_calendar_invite` | body | `boolean` | no | Send a calendar invitation when true. |
| `send_notification` | body | `boolean` | no | Send a mobile push notification when true; documented for immediate dispatches. |
| `no_form_assignment` | body | `boolean` | no | Allow creation without the assignee being assigned to the form when true. |
| `repeat_interval` | body | `list` | no | Required for recurring dispatches. Accepted values: `daily`, `monthly_date`, `monthly_day`, `weekdays`, `weekly`, `yearly`. |
| `repeat_ends_option` | body | `list` | no | Required for recurring dispatches. Accepted values: `ends_after`, `ends_on`. |
| `repeat_ends_on` | body | `string` | no | Required when repeat ends option is ends_on; format MM/DD/YYYY. |
| `repeat_occurrences` | body | `number` | no | Required when repeat ends option is ends_after. |
