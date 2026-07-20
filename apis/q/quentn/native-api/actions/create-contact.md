# Create Contact with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/contact`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Create Contact](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact.mail` | body | `string` | yes | Valid email address for the new Quentn contact. |
| `contact.first_name` | body | `string` | no | Contact first name. |
| `contact.family_name` | body | `string` | no | Contact last name. |
| `contact.ba_street` | body | `string` | no | Billing or street address. |
| `contact.ba_city` | body | `string` | no | City for the full-address fallback. |
| `contact.ba_postal_code` | body | `string` | no | Postal code for the full-address fallback. |
| `contact.comment` | body | `string` | no | Optional comment to add while creating the contact. |
| `contact.request_ip` | body | `string` | no | IPv4 address associated with the contact submission. Required when flood protection options are used. |
| `duplicate_check_method` | body | `string` | no | How Quentn should check for duplicates: auto, email, or none. |
| `duplicate_merge_method` | body | `string` | no | How Quentn should merge duplicate contacts: update_add, update, or add. |
| `flood_limit` | body | `number` | no | Maximum number of contacts allowed from the same request IP within an hour. |
| `spam_protection` | body | `boolean` | no | Whether Quentn should check the request IP against a spam database. |
