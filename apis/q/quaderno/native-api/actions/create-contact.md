# Create Contact with Quaderno

Creates a new contact in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Contact](https://developers.quaderno.io/api/#tag/Contacts/operation/createContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | City for the contact. |
| `contact_person` | body | `string` | no | Named contact person. |
| `country` | body | `string` | no | Two-letter country code for the contact. |
| `department` | body | `string` | no | Department name. |
| `first_name` | body | `string` | yes | Contact first name. |
| `full_name` | body | `string` | no | Full name for the contact. |
| `kind` | body | `string` | no | Whether the contact is a company or person. |
| `language` | body | `string` | no | Preferred language code. |
| `last_name` | body | `string` | no | Contact last name. |
| `notes` | body | `string` | no | Internal notes for the contact. |
| `phone_1` | body | `string` | no | Primary phone number. |
| `postal_code` | body | `string` | no | Postal code for the contact. |
| `processor` | body | `string` | no | External processor name for the contact. |
| `processor_id` | body | `string` | no | External processor identifier for the contact. |
| `region` | body | `string` | no | Region or state for the contact. |
| `street_line_1` | body | `string` | no | Primary street address. |
| `street_line_2` | body | `string` | no | Secondary street address. |
| `tax_id` | body | `string` | no | Contact tax identification number. |
| `tax_status` | body | `string` | no | Tax treatment for the contact. |
| `web` | body | `string` | no | Contact website URL. |
| `email` | body | `string` | no | Contact email address. |
