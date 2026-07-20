# Get Contact List with Constant Contact

Retrieves a contact list from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact_lists/:list_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Get Contact List](https://developer.constantcontact.com/api_guide/lists_get_single.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | Unique ID of the contact list to retrieve. |
| `include_membership_count` | query | `string` | no | Include membership totals (`active` or `all`). |
