# Update Ticket with Syncro

Updates an existing ticket in Syncro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:id`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Update Ticket](https://api-docs.syncromsp.com/#/Ticket/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro ticket ID. |
| `customer_id` | body | `number` | no | — |
| `ticket_type_id` | body | `number` | no | — |
| `number` | body | `string` | no | — |
| `subject` | body | `string` | yes | — |
| `due_date` | body | `date` | no | — |
| `start_at` | body | `date` | no | — |
| `end_at` | body | `date` | no | — |
| `location_id` | body | `number` | no | — |
| `problem_type` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `user_id` | body | `number` | no | — |
| `properties` | body | `object` | no | — |
| `asset_ids[]` | body | `array<number>` | no | — |
| `signature_name` | body | `string` | no | — |
| `signature_data` | body | `string` | no | — |
| `sla_id` | body | `number` | no | — |
| `contact_id` | body | `number` | no | — |
| `priority` | body | `string` | no | — |
| `outtake_form_data` | body | `string` | no | — |
| `outtake_form_date` | body | `date` | no | — |
| `outtake_form_name` | body | `string` | no | — |
| `tag_list[]` | body | `array<string>` | no | — |
| `comments_attributes[]` | body | `array<object>` | no | — |
