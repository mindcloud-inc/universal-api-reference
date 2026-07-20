# Submit Form JSON with Formspark

Creates a Formspark form submission from a JSON payload.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form JSON](https://documentation.formspark.io/examples/ajax.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID from the hosted endpoint URL, for example `your-form-id` in `https://submit-form.com/your-form-id`. |
| `email` | body | `string` | no | Optional email field to include in the submission body. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `name` | body | `string` | no | Optional display name field to include in the submission body. |
