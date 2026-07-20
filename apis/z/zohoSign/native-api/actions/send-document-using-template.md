# Send Document Using Template with Zoho Sign

Creates a document from a template in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:templateId/createdocument`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Send Document Using Template](https://www.zoho.com/sign/api/template-managment/send-documents-using-template.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Zoho Sign template identifier. |
| `data` | body | `object` | yes | Zoho Sign template-send payload wrapper. |
| `data.templates` | body | `object` | yes | Template send details. |
| `data.templates.request_name` | body | `string` | no | Document request name. Defaults to the template name when omitted. |
| `data.templates.field_data` | body | `object` | no | Prefill values for template fields as a JSON object. |
| `data.templates.actions[]` | body | `array<object>` | yes | Recipient rows aligned to the template actions. |
| `data.templates.actions[].action_id` | body | `string` | yes | Template action identifier for the recipient row. |
| `data.templates.actions[].action_type` | body | `string` | no | Recipient action type such as SIGN. |
| `data.templates.actions[].role` | body | `string` | no | Template role name for the recipient row. |
| `data.templates.actions[].recipient_name` | body | `string` | yes | Recipient full name. |
| `data.templates.actions[].recipient_email` | body | `string` | yes | Recipient email address. |
| `data.templates.actions[].in_person_name` | body | `string` | no | Host name for in-person signing flows. |
| `data.templates.actions[].in_person_email` | body | `string` | no | Host email for in-person signing flows. |
| `data.templates.actions[].private_notes` | body | `string` | no | Private instructions for a specific recipient. |
| `data.templates.actions[].verify_recipient` | body | `boolean` | yes | Whether recipient verification is required. |
| `data.templates.actions[].verification_type` | body | `string` | no | Recipient verification mode such as EMAIL. |
| `data.templates.notes` | body | `string` | no | Common message sent to all recipients. |
| `is_quicksend` | body | `boolean` | no | When true, immediately send the created request for signature. |
