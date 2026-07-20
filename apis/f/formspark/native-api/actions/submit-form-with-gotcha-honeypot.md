# Submit Form With Gotcha Honeypot with Formspark

Creates a Formspark form submission with a gotcha honeypot field.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Gotcha Honeypot](https://documentation.formspark.io/setup/spam-protection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `_gotcha` | body | `string` | yes | Leave this field empty for legitimate submissions. |
