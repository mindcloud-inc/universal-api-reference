# Submit Form With Nested Email Object with Formspark

Creates a Formspark form submission with nested email settings.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Nested Email Object](https://documentation.formspark.io/examples/ajax.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `_email.subject` | body | `string` | yes | Notification email subject inside the nested `_email` object. |
| `_email.from` | body | `string` | no | Sender display name inside the nested `_email` object. |
| `_email.template.title` | body | `string` | no | Title inside the nested `_email.template` object. |
| `_email.template.footer` | body | `string` | no | Footer toggle inside the nested `_email.template` object. |
