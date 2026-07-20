# Create Template with Zoho Sign

Creates a template in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Create Template](https://www.zoho.com/sign/api/template-managment/create-template.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file to upload as the template source document. |
| `data` | body | `object` | yes | Zoho Sign template payload wrapper. |
| `data.templates` | body | `object` | yes | Template details. |
| `data.templates.template_name` | body | `string` | yes | Name of the template. |
| `data.templates.request_type_id` | body | `string` | no | Document category identifier for the template. |
| `data.templates.notes` | body | `string` | no | Common message sent to all recipients. |
| `data.templates.expiration_days` | body | `number` | no | Number of days before documents from this template expire. |
| `data.templates.is_sequential` | body | `boolean` | no | Whether signers must act in order. |
| `data.templates.email_reminders` | body | `boolean` | no | Whether reminder emails are enabled. |
| `data.templates.reminder_period` | body | `number` | no | Reminder frequency in days. |
| `data.templates.folder_id` | body | `string` | no | Folder identifier where the template should be stored. |
| `data.templates.actions[]` | body | `array<object>` | no | Role rows for the template. |
| `data.templates.actions[].action_type` | body | `string` | no | Role action type such as SIGN. |
| `data.templates.actions[].role` | body | `string` | no | Template role name such as Signer. |
| `data.templates.actions[].recipient_name` | body | `string` | no | Recipient full name for the role. |
| `data.templates.actions[].recipient_email` | body | `string` | no | Recipient email address for the role. |
| `data.templates.actions[].in_person_name` | body | `string` | no | Host name for in-person signing roles. |
| `data.templates.actions[].in_person_email` | body | `string` | no | Host email for in-person signing roles. |
| `data.templates.actions[].signing_order` | body | `number` | no | Sequential order number for the role. |
| `data.templates.actions[].verify_recipient` | body | `boolean` | no | Whether recipients in this role must be verified. |
| `data.templates.actions[].verification_type` | body | `string` | no | Verification method such as EMAIL. |
| `data.templates.actions[].verification_code` | body | `string` | no | Verification code when required. |
| `data.templates.actions[].private_notes` | body | `string` | no | Private instructions for this role. |
