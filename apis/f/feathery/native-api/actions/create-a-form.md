# Create a Form with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Create a Form](https://api-docs.feathery.io/#create-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_name` | body | `string` | yes | The unique name of the new form. |
| `template_form_id` | body | `string` | yes | The ID of the template form to copy from. |
| `steps[]` | body | `array<object>` | yes | An array of steps to create in the new form. |
| `navigation_rules[]` | body | `array<object>` | yes | An array of navigation rules connecting the steps. |
| `logic_rules[]` | body | `array<object>` | no | An array of advanced logic rules to associate with the form. |
| `enabled` | body | `boolean` | no | Whether the created form should be enabled. If omitted, it inherits the template form status. |
