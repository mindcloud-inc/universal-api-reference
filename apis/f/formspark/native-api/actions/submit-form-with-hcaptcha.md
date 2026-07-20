# Submit Form With hCaptcha with Formspark

Creates a Formspark form submission with hCaptcha validation.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With hCaptcha](https://documentation.formspark.io/setup/spam-protection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `h-captcha-response` | body | `string` | no | hCaptcha challenge response token. |
