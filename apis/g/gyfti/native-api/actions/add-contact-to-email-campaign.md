# Add Contact to Email Campaign with gyfti

Adds a contact to an email campaign in gyfti.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/1_zapier_add_contact_trigger/`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Add Contact to Email Campaign](https://developer.gyfti.fr/automate-your-gifts/add-contact-to-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | body | `string` | yes | The gyfti trigger campaign ID to add the contact to. |
| `contact_email` | body | `string` | yes | Recipient email address. |
| `contact_firstname` | body | `string` | yes | Recipient first name. |
| `contact_lastname` | body | `string` | yes | Recipient last name. |
| `company` | body | `string` | no | Recipient company name. |
| `jobtitle` | body | `string` | no | Recipient job title. |
| `phone` | body | `string` | no | Recipient phone number. |
| `address` | body | `string` | no | Recipient street address. |
| `additional_address` | body | `string` | no | Recipient additional address details. |
| `postal_code` | body | `string` | no | Recipient postal code. |
| `city` | body | `string` | no | Recipient city. |
| `country` | body | `string` | no | Recipient country. |
