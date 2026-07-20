# Create Lead with noCRM.io

Creates a new lead in noCRM.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Create Lead](https://www.nocrm.io/api#create-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | body | `date` | no | Backdate the lead creation time. |
| `description` | body | `string` | yes | Lead description, usually contact information and notes. |
| `step` | body | `string` | no | Step name or step ID for the lead. |
| `tags` | body | `list<string>` | no | Tags to attach to the lead. Send multiple values as a string separated by `,`. |
| `title` | body | `string` | yes | Lead title, usually the company name. |
| `user_id` | body | `string` | no | Optional user ID or email for direct assignment. |
