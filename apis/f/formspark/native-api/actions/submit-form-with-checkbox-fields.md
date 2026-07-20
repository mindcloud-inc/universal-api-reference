# Submit Form With Checkbox Fields with Formspark

Creates a Formspark form submission with checkbox fields.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Checkbox Fields](https://documentation.formspark.io/html-form/special-input-types.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `has-bike` | body | `string` | no | Example checked checkbox field value. |
| `has-car` | body | `string` | no | Example checked checkbox field value. |
