# Update Contact with Anyleads

Updates an existing contact in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/update-a-contact`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Update Contact](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_name` | body | `string` | no | List name for the contact. |
| `sub_owner` | body | `string` | no | List or campaign owner email. |
| `email` | body | `string` | yes | Primary contact email. |
| `score` | body | `number` | no | Lead score. |
| `title` | body | `string` | no | Contact title. |
| `first_name` | body | `string` | no | Contact first name. |
| `middle_name` | body | `string` | no | Contact middle name. |
| `last_name` | body | `string` | no | Contact last name. |
| `job_title` | body | `string` | no | Contact job title. |
| `phone` | body | `string` | no | Contact phone number. |
| `other_email` | body | `string` | no | Secondary contact email. |
| `linkedin_url` | body | `string` | no | LinkedIn profile URL. |
| `keywords` | body | `string` | no | Keywords associated with the contact. |
| `description` | body | `string` | no | Contact description. |
| `city` | body | `string` | no | Contact city. |
| `region` | body | `string` | no | Contact region. |
| `postal_code` | body | `string` | no | Contact postal code. |
| `country` | body | `string` | no | Contact country. |
| `company_name` | body | `string` | no | Related company name. |
| `company_domain` | body | `string` | no | Related company domain. |
| `company_website` | body | `string` | no | Related company website. |
| `company_phone` | body | `string` | no | Related company phone. |
| `company_industry` | body | `string` | no | Related company industry. |
| `company_size` | body | `string` | no | Related company size. |
| `company_type` | body | `string` | no | Related company type. |
| `company_address` | body | `string` | no | Related company address. |
