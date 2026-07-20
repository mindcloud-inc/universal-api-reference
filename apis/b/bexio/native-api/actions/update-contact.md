# Update Contact with Bexio

Updates a contact in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/contact/:contact_id`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Update Contact](https://docs.bexio.com/#tag/Contacts/operation/v2EditContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The id of the contact. |
| `contact_type_id` | body | `number` | yes | Use 1 for companies or 2 for persons. |
| `name_1` | body | `string` | yes | Company name when contact type is company, otherwise last name. |
| `name_2` | body | `string` | no | Company addition when contact type is company, otherwise first name. |
| `mail` | body | `string` | no | Primary email address. |
| `phone_mobile` | body | `string` | no | Mobile phone number. |
| `street_name` | body | `string` | no | Required if house number or address addition is provided. |
| `house_number` | body | `string` | no | Requires street name when provided. |
| `address_addition` | body | `string` | no | Requires street name when provided. |
| `postcode` | body | `string` | no | Postal code. |
| `city` | body | `string` | no | City. |
| `country_id` | body | `number` | no | References a country object. |
| `user_id` | body | `number` | yes | References a user object. |
| `owner_id` | body | `number` | yes | Owner id. |
| `nr` | body | `string` | no | If set to null, the number will be assigned automatically. Must be a number, can also be used as integer. |
| `salutation_id` | body | `number` | no | References a salutation object. |
| `salutation_form` | body | `number` | no | Salutation form value. |
| `title_id` | body | `number` | no | References a title object. |
| `birthday` | body | `date` | no | Birthday date. |
| `mail_second` | body | `string` | no | Secondary email address. |
| `phone_fixed` | body | `string` | no | Primary fixed phone number. |
| `phone_fixed_second` | body | `string` | no | Secondary fixed phone number. |
| `fax` | body | `string` | no | Fax number. |
| `url` | body | `string` | no | Website URL. |
| `skype_name` | body | `string` | no | Skype name. |
| `remarks` | body | `string` | no | Remarks. |
| `language_id` | body | `number` | no | References a language object. |
| `contact_group_ids` | body | `string` | no | References one or more contact group objects. Send multiple values as a string separated by `,`. |
| `contact_branch_ids` | body | `string` | no | References one or more contact sector objects. Send multiple values as a string separated by `,`. |
