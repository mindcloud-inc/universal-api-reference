# Update Template with Superchat

Updates an existing template in Superchat.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/templates/{template_id}`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Update Template](https://developers.superchat.com/reference/updatetemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The unique identifier of the template |
| `name` | body | `string` | no | Internal name of the template |
| `folder_id` | body | `string` | no | The ID of the folder this template should be save in. |
| `file_ids[]` | body | `array<string>` | no | — |
