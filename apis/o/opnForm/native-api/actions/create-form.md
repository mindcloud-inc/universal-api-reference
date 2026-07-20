# Create Form with OpnForm

Creates a new form in OpnForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/forms`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Create Form](https://docs.opnform.com/api-reference/forms/create-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | Workspace ID that will own the form. |
| `title` | body | `string` | yes | Human-readable form title. |
| `visibility` | body | `string` | yes | Form visibility state. |
| `language` | body | `string` | yes | Two-letter ISO language code. |
| `properties` | body | `object` | yes | JSON array of form blocks and fields. |
