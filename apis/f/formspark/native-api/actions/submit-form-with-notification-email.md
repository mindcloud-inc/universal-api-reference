# Submit Form With Notification Email with Formspark

Creates a Formspark form submission with notification email settings.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Notification Email](https://documentation.formspark.io/customization/notification-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `_email.subject` | body | `string` | no | Custom subject line for the notification email. |
| `_email.from` | body | `string` | no | Custom sender name for the notification email. |
| `_email.template.title` | body | `string` | no | Custom title for the default notification email template. |
| `_email.template.footer` | body | `string` | no | Set to false to hide the default notification email footer. |
