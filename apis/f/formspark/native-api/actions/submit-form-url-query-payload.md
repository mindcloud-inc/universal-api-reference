# Submit Form URL Query Payload with Formspark

Creates a Formspark form submission from query parameters.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form URL Query Payload](https://documentation.formspark.io/examples/ajax.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `email` | query | `string` | no | Optional email value submitted through the query string. |
| `message` | query | `string` | no | Optional message value submitted through the query string. |
