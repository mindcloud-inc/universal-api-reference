# List Contacts with Constant Contact

Retrieves contact records from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [List Contacts](https://developer.constantcontact.com/api_guide/contacts_get_collection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Search contacts by a specific email address. |
| `status` | query | `string` | no | Filter contacts by lifecycle status. |
| `lists` | query | `string` | no | Filter contacts by one or more contact list IDs. |
| `segment_id` | query | `string` | no | Return contacts that match a specific segment ID. |
| `tags` | query | `string` | no | Filter contacts by one or more tag IDs. |
| `updated_after` | query | `date` | no | Return contacts updated after this datetime (ISO-8601). |
| `updated_before` | query | `date` | no | Return contacts updated before this datetime (ISO-8601). |
| `created_after` | query | `date` | no | Return contacts created after this datetime (ISO-8601). |
| `created_before` | query | `date` | no | Return contacts created before this datetime (ISO-8601). |
| `optout_after` | query | `date` | no | Return contacts that opted out after this datetime (ISO-8601). |
| `optout_before` | query | `date` | no | Return contacts that opted out before this datetime (ISO-8601). |
| `include` | query | `string` | no | Include specific contact sub-resources in the response. |
| `sms_status` | query | `string` | no | Filter contacts by SMS consent status. |
| `include_count` | query | `boolean` | no | Include total matching contacts count in response metadata. |
