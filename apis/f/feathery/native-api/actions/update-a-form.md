# Update a Form with Feathery

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/form/:form_id/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Update a Form](https://api-docs.feathery.io/#update-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form to update. |
| `enabled` | body | `boolean` | no | Whether the form should be enabled or disabled. |
| `form_name` | body | `string` | no | The new name to set for the form. |
| `translations` | body | `object` | no | A mapping of default text to translations. |
| `integrations[]` | body | `array<object>` | no | An array of integrations created in this form. |
