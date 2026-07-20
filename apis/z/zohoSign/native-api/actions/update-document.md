# Update Document with Zoho Sign

Updates an existing document in Zoho Sign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/requests/:requestId`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Update Document](https://www.zoho.com/sign/api/document-managment/update-document.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Zoho Sign request identifier. |
| `data` | body | `object` | no | Zoho Sign update payload wrapper. |
| `data.requests` | body | `object` | no | Updated signature request details. |
| `data.requests.request_name` | body | `string` | no | Updated display name for the signature request. |
| `data.requests.notes` | body | `string` | no | Notes included with the request. |
| `data.requests.description` | body | `string` | no | Description of the request. |
| `data.requests.expiration_days` | body | `number` | no | Number of days before the request expires. |
| `data.requests.is_sequential` | body | `boolean` | no | Whether recipients must sign in order. |
| `data.requests.email_reminders` | body | `boolean` | no | Whether reminder emails are enabled. |
| `data.requests.reminder_period` | body | `number` | no | Reminder frequency in days. |
| `data.requests.validity` | body | `number` | no | Validity setting for the request. |
| `data.requests.actions[]` | body | `array<object>` | no | Recipients to update on the request. |
| `data.requests.actions[].action_id` | body | `string` | no | Existing Zoho Sign action identifier for the recipient row. |
| `data.requests.actions[].recipient_name` | body | `string` | no | Recipient display name. |
| `data.requests.actions[].recipient_email` | body | `string` | no | Recipient email address. |
| `data.requests.actions[].action_type` | body | `string` | no | Recipient action type such as SIGN. |
| `data.requests.actions[].private_notes` | body | `string` | no | Private instructions shown to the recipient. |
| `data.requests.actions[].signing_order` | body | `number` | no | Sequential order number for the recipient. |
| `data.requests.actions[].is_bulk` | body | `boolean` | no | Whether the recipient row is part of a bulk send. |
| `data.requests.actions[].verify_recipient` | body | `boolean` | no | Whether Zoho Sign should verify the recipient before signing. |
