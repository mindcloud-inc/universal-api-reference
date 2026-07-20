# Create Form with Dashform

Creates a form in Dashform.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/forms`
- **Base URL:** `https://getaiform.com`
- **Official documentation:** [Create Form](https://github.com/makloai/dashform-cli-docs#forms-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional form description. |
| `name` | body | `string` | yes | Form name. |
| `tone` | body | `string` | no | Optional tone or style for the form. |
| `type` | body | `string` | no | Form type: structured or dynamic. |
