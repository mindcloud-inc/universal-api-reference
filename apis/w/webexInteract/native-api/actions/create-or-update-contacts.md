# Create or update contacts with Webex Interact

Creates or updates contacts in Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/v1/contacts`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Create or update contacts](https://docs.webexinteract.com/reference/contacts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | URL to receive a webhook when contact creation processing completes. |
| `correlation_id` | body | `string` | no | Correlation ID returned on the contact completion callback webhook. |
| `list_id` | body | `string` | yes | ID of the list where contacts are added or updated. |
| `phone_region` | body | `string` | no | Default phone region, such as GB. |
| `merge_type` | body | `string` | yes | Merge behavior: skipDuplicates, allowDuplicates, mergeByPhoneNumberInList, or mergeByWhatsappIdInList. |
| `contacts` | body | `list<object>` | yes | Array of contact objects. Each contact must include phone_number or whatsapp_number. |
