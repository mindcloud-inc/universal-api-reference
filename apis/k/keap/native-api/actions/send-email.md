# Send Email with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/emails:send`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Send Email](https://developer.keap.com/docs/restv2/#tag/Email/operation/sendEmail)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address_field` | body | `string` | no |
| `attachments` | body | `string` | no |
| `contacts` | body | `string` | yes |
| `html_content` | body | `string` | no |
| `plain_content` | body | `string` | no |
| `subject` | body | `string` | yes |
| `user_id` | body | `string` | yes |
