# Submit Form With Honeypot with Formspark

Creates a Formspark form submission with a honeypot field.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Honeypot](https://documentation.formspark.io/setup/spam-protection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `_honeypot` | body | `string` | yes | Leave this field empty for legitimate submissions. |
