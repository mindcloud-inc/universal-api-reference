# Update Lead with noCRM.io

Updates an existing lead in noCRM.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:id`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Update Lead](https://www.nocrm.io/api#update-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | no | New amount for the lead. |
| `append_desc` | body | `string` | no | Text to append to the end of the lead description. |
| `created_at` | body | `date` | no | Backdate the lead creation time. |
| `description` | body | `string` | no | New description for the lead. |
| `estimated_closing_date` | body | `date` | no | Estimated closing date for the lead. |
| `fields[]` | body | `array<object>` | no | Field values to update inside the lead description. |
| `id` | path | `string` | yes | The identifier of the lead. |
| `probability` | body | `number` | no | New probability for the lead. |
| `remind_date` | body | `date` | no | Reminder date when setting standby status or a reminder. |
| `remind_time` | body | `string` | no | Reminder time in 24-hour format. |
| `reminder_activity_id` | body | `string` | no | Activity ID to use for the reminder. |
| `reminder_duration` | body | `number` | no | Reminder duration in minutes. |
| `reminder_note` | body | `string` | no | Note to attach to the reminder. |
| `starred` | body | `boolean` | no | Whether the lead is starred. |
| `status` | body | `string` | no | New status for the lead. |
| `step` | body | `string` | no | New step name or step ID for the lead. |
| `tags` | body | `list<string>` | no | Tags to apply to the lead. Send multiple values as a string separated by `,`. |
| `title` | body | `string` | no | New title for the lead. |
| `user_id` | body | `string` | no | New user ID or email for the lead. |
