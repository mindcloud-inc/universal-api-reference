# Submit Form With Error Redirect with Formspark

Creates a Formspark form submission with success and error redirects.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Error Redirect](https://documentation.formspark.io/customization/redirection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `email` | body | `string` | no | Optional email field to include in the submission body. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `_redirect` | body | `string` | no | Custom success redirect URL. |
| `_error` | body | `string` | no | Custom error redirect URL. |
