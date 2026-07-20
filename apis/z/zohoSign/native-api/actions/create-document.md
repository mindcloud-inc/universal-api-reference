# Create Document with Zoho Sign

Creates a document in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Create Document](https://www.zoho.com/sign/api/document-managment/create-document.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file to upload for the signature request. |
| `data` | body | `object` | no | Zoho Sign request payload wrapper. |
| `data.requests` | body | `object` | no | Signature request details. |
| `data.requests.request_name` | body | `string` | yes | Display name for the signature request. |
| `data.requests.expiration_days` | body | `number` | no | Number of days before the request expires. |
| `data.requests.is_sequential` | body | `boolean` | no | Whether recipients must sign in order. |
| `data.requests.email_reminders` | body | `boolean` | no | Whether reminder emails are enabled. |
| `data.requests.reminder_period` | body | `number` | no | Reminder frequency in days. |
| `data.requests.actions[]` | body | `array<object>` | no | Recipients that will act on the document. |
| `data.requests.actions[].recipient_name` | body | `string` | no | Recipient display name. |
| `data.requests.actions[].recipient_email` | body | `string` | no | Recipient email address. |
| `data.requests.actions[].action_type` | body | `string` | no | Recipient action type such as SIGN. |
| `data.requests.actions[].signing_order` | body | `number` | no | Sequential order number for the recipient. |
| `data.requests.actions[].verify_recipient` | body | `boolean` | no | Whether Zoho Sign should verify the recipient before signing. |
| `data.requests.actions[].verification_type` | body | `string` | no | Recipient verification method such as EMAIL. |
| `data.requests.actions[].verification_code` | body | `string` | no | Verification code sent to the recipient when required. |
| `data.requests.actions[].private_notes` | body | `string` | no | Private instructions shown to the recipient. |
