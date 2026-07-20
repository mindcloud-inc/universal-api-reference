# Create Contact with Yousign

Creates a new contact in Yousign.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Create Contact](https://developers.yousign.com/reference/post-contact-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Contact first name. |
| `last_name` | body | `string` | yes | Contact last name. |
| `email` | body | `string` | yes | Contact email address. |
| `locale` | body | `string` | yes | Contact locale. |
| `phone_number` | body | `string` | no | Contact phone number in E.164 format. |
| `company_name` | body | `string` | no | Company name for the contact. |
| `job_title` | body | `string` | no | Job title for the contact. |
| `workspace_id` | body | `string` | no | Workspace ID to associate with the contact. |
| `address_line_1` | body | `string` | no | Primary street address line. |
| `address_line_2` | body | `string` | no | Secondary street address line. |
| `address_city` | body | `string` | no | City for the contact address. |
| `address_postal_code` | body | `string` | no | Postal code for the contact address. |
| `address_country` | body | `string` | no | Country for the contact address. |
