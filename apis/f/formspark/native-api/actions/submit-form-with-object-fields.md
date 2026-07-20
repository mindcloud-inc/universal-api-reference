# Submit Form With Object Fields with Formspark

Creates a Formspark form submission with object fields.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Object Fields](https://documentation.formspark.io/setup/arrays-and-objects.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `contact.name` | body | `string` | yes | Dotted object field for a nested contact name. |
| `contact.email` | body | `string` | no | Dotted object field for a nested contact email. |
| `company.name` | body | `string` | no | Dotted object field for a nested company name. |
