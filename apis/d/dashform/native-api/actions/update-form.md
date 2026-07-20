# Update Form with Dashform

Updates a form in Dashform.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/forms/:id`
- **Base URL:** `https://getaiform.com`
- **Official documentation:** [Update Form](https://github.com/makloai/dashform-cli-docs#forms-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | New form description. |
| `id` | path | `string` | yes | Dashform form ID or public ID. |
| `name` | body | `string` | no | New form name. |
| `tone` | body | `string` | no | New tone or style. |
| `type` | body | `string` | no | New form type: structured or dynamic. |
