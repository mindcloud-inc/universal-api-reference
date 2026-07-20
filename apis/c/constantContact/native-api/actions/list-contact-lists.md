# List Contact Lists with Constant Contact

Retrieves contact lists from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact_lists`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [List Contact Lists](https://developer.constantcontact.com/api_guide/lists_get_all.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_count` | query | `boolean` | no | Include total number of matching contact lists. |
| `include_membership_count` | query | `string` | no | Include list membership totals (`active` or `all`). |
| `name` | query | `string` | no | Filter by exact contact list name. |
| `status` | query | `string` | no | Filter by list status. |
| `channel_type` | query | `string` | no | Filter by channel type (`email` or `sms`). |
| `include_sms_membership_count` | query | `boolean` | no | Include SMS member totals when channel type is `sms`. |
