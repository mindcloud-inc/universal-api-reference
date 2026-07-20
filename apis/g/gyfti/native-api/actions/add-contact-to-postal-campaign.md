# Add Contact to Postal Campaign with gyfti

Adds a contact to a postal campaign in gyfti.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/1_zapier_add_contact_trigger_directe/`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Add Contact to Postal Campaign](https://developer.gyfti.fr/automate-your-gifts/add-contact-to-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | body | `string` | yes | The gyfti postal trigger campaign ID to add the contact to. |
| `contact_email` | body | `string` | yes | Recipient email address. |
| `contact_fistname` | body | `string` | yes | Recipient first name. gyfti's postal endpoint documents this external key as contact_fistname. |
| `contact_lastname` | body | `string` | yes | Recipient last name. |
| `address` | body | `string` | yes | Recipient street address. |
| `phone` | body | `string` | yes | Recipient phone number. |
| `city` | body | `string` | yes | Recipient city. |
| `postal_code` | body | `string` | yes | Recipient postal code. |
| `country` | body | `string` | yes | Recipient country. |
| `additional_address` | body | `string` | no | Recipient additional address details. |
| `jobtitle` | body | `string` | no | Recipient job title. |
