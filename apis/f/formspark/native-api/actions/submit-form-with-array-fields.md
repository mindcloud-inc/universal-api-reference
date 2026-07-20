# Submit Form With Array Fields with Formspark

Creates a Formspark form submission with array fields.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Array Fields](https://documentation.formspark.io/setup/arrays-and-objects.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `items[0]` | body | `string` | yes | First indexed array element. |
| `items[1]` | body | `string` | yes | Second indexed array element. |
