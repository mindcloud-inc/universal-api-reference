# Create Contact with ClickSend SMS

Creates a new contact in a ClickSend SMS list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/lists/:list_id/contacts`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Create Contact](https://developers.clicksend.com/docs/contacts/lists/other/create-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List identifier. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Items per page. |
| `phone_number` | body | `string` | yes | Contact phone number. |
| `email` | body | `string` | no | Contact email. |
| `fax_number` | body | `string` | no | Contact fax number. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `address_line_1` | body | `string` | no | Address line 1. |
| `address_line_2` | body | `string` | no | Address line 2. |
| `address_city` | body | `string` | no | Address city. |
| `address_state` | body | `string` | no | Address state. |
| `address_postal_code` | body | `string` | no | Address postal code. |
| `address_country` | body | `string` | no | Address country code. |
| `organization_name` | body | `string` | no | Organization name. |
| `custom_1` | body | `string` | yes | Custom field 1. |
| `custom_2` | body | `string` | no | Custom field 2. |
| `custom_3` | body | `string` | no | Custom field 3. |
| `custom_4` | body | `string` | no | Custom field 4. |
