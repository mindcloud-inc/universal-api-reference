# Update task template with Vibrato

Updates an existing task template in Vibrato.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/task_templates/{uuid}/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Update task template](https://docs.getvibrato.com/api-reference/tasktemplates/update-an-existing-task-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID from Vibrato. |
| `task_name` | body | `string` | no | Task template name. |
| `task_description` | body | `string` | no | Task template description. |
| `task_instructions` | body | `string` | no | Instructions for the task template. |
| `task_properties[]` | body | `array<object>` | no | Task property definitions. |
| `recipient_name` | body | `string` | no | Default recipient name. |
| `recipient_phone_number` | body | `string` | no | Default recipient phone number. |
| `recipient_country_code` | body | `string` | no | Default recipient country code. |
| `call_locale` | body | `string` | no | Default call locale. |
| `public` | body | `boolean` | no | Whether the template is public. |
| `featured` | body | `boolean` | no | Whether the template is featured. |
| `tags[]` | body | `array<string>` | no | Tags. |
| `iconoir_icon` | body | `string` | no | Iconoir icon name. |
