# Create Action with SafetyCulture

Creates a new action in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/actions`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Create Action](https://developer.safetyculture.com/reference/actionsservice_createaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | no | The unique identifier of the action If not provided, UUID will be generated server side. |
| `title` | body | `string` | yes | Required. Title of the action Title is limited to only 255 characters max. |
| `description` | body | `string` | no | Description of the action (maximum 30000 characters). |
| `collaborators[]` | body | `array<object>` | no | The collaborators involved into this action. |
| `priority_id` | body | `string` | no | ID of the action's priority If not set, this action will be stored with the default priority(none). |
| `status_id` | body | `string` | no | ID of the action's status If not set, this action will be stored with the default status(to do). |
| `created_at` | body | `date` | no | Date and time this action was created. |
| `due_at` | body | `date` | no | Date/time this action is due |
| `inspection_id` | body | `string` | no | ID of the inspection the action belongs to If not set, this action is a standalone action and the inspection ID will be null. |
| `inspection_item_id` | body | `string` | no | ID of the item in the inspection associated with the action |
| `template_id` | body | `string` | no | If a template ID is provided then an inspection ID must be provided. If not set, this action is a standalone action and the template ID will be null. |
| `site_id` | body | `string` | no | ID of the Site associated with the action. |
| `references[]` | body | `array<object>` | no | Array of references attached to this action. |
| `asset_id` | body | `string` | no | ID of the Asset associated with the action |
| `label_ids[]` | body | `array<string>` | no | IDs of the labels associated with the action. |
| `type` | body | `object` | no | The type to create an action in. |
| `field_values[]` | body | `array<object>` | no | Array of custom fields and their values to create with the action. |
| `template_ids[]` | body | `array<string>` | no | The list of templates to be linked to the action. |
