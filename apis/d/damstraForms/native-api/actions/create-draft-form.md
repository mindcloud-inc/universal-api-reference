# Create Draft Form with Damstra Forms

Creates a draft form in Damstra Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Draft Form](https://sammapi.docs.apiary.io/#reference/forms/form-collection/create-a-draft-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_template_id` | body | `number` | yes | Draft template identifier for the new form. |
| `project_id` | body | `number` | yes | Project identifier for the new form. |
| `created_by_user_id` | body | `number` | yes | User identifier to record as the form creator. |
| `fields[]` | body | `array<object>` | yes | Field values for the form, using Damstra field_reference values. |
