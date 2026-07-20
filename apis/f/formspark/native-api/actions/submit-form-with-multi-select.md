# Submit Form With Multi Select with Formspark

Creates a Formspark form submission with multiple selected values.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Multi Select](https://documentation.formspark.io/html-form/drop-down-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `cars[0]` | body | `string` | yes | First selected option. |
| `cars[1]` | body | `string` | yes | Second selected option. |
