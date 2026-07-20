# Submit Form With Uploadcare File Link with Formspark

Creates a Formspark form submission with an Uploadcare file URL.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Uploadcare File Link](https://documentation.formspark.io/setup/file-uploads.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `photo` | body | `string` | yes | Uploadcare-hosted file URL returned by the upload widget. |
| `message` | body | `string` | no | Optional message alongside the file link. |
