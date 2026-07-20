# Send Email Operational Message to Contacts with ActiveTrail

Sends an operational email to contacts in ActiveTrail.

## Endpoint

- **Method:** `POST`
- **Path:** `/OperationalMessage/Contacts`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Send Email Operational Message to Contacts](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-OperationalMessage-Contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | body | `object` | no | BCC emails. |
| `bcc.bcc_emails[]` | body | `array<string>` | no | — |
| `contact_package[]` | body | `array<object>` | no | Email addresses with per-contact key/value pairs. |
| `contact_package[].contact` | body | `object` | no | — |
| `contact_package[].contact.email` | body | `string` | no | — |
| `contact_package[].contact.first_name` | body | `string` | no | — |
| `contact_package[].contact.last_name` | body | `string` | no | — |
| `contact_package[].contact.sms` | body | `string` | no | — |
| `contact_package[].pairs[]` | body | `array<object>` | no | — |
| `contact_package[].pairs[].key` | body | `string` | no | — |
| `contact_package[].pairs[].value` | body | `string` | no | — |
| `design` | body | `object` | yes | Message design. |
| `design.add_print_button` | body | `boolean` | no | — |
| `design.add_Statistics` | body | `boolean` | no | — |
| `design.content` | body | `string` | no | — |
| `design.language_type` | body | `string` | no | — |
| `design.template_id` | body | `number` | no | — |
| `details` | body | `object` | yes | Message details. |
| `details.classification` | body | `string` | no | — |
| `details.name` | body | `string` | no | — |
| `details.subject` | body | `string` | no | — |
| `details.user_profile_fromname` | body | `string` | no | — |
| `details.user_profile_id` | body | `number` | no | — |
