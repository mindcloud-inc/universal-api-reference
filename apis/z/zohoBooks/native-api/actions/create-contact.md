# Create Contact with Zoho Books

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Create Contact](https://www.zoho.com/books/api/v3/contacts/#create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_name` | body | `string` | yes | Display name for the contact. |
| `contact_type` | body | `list` | no | Determines whether the contact is a customer or vendor. Accepted values: `customer`, `vendor`. |
| `company_name` | body | `string` | no | Legal or registered company name for the contact. |
| `website` | body | `string` | no | Official website URL of the contact. |
| `language_code` | body | `list` | no | Preferred language for the contact. Accepted values: `de`, `en`, `en_gb`, `es`, `fr`, `it`, `ja`, `nl`, `pt`, `pt_br`, `sv`, `zh`. |
| `customer_sub_type` | body | `list` | no | Additional classification for customer contacts. Accepted values: `business`, `individual`. |
| `credit_limit` | body | `number` | no | Maximum credit amount allowed for the customer. |
| `contact_number` | body | `string` | no | Internal contact number. |
| `payment_terms` | body | `number` | no | Number of days allowed for payment. |
| `notes` | body | `string` | no | Additional notes about the contact. |
| `billing_address` | body | `object` | no | Billing address information for the contact. |
| `billing_address.address` | body | `string` | no | Street address line 1 for the billing address. |
| `billing_address.city` | body | `string` | no | City for the billing address. |
| `billing_address.state` | body | `string` | no | State for the billing address. |
| `billing_address.zip` | body | `string` | no | Postal code for the billing address. |
| `billing_address.country` | body | `string` | no | Country for the billing address. |
| `contact_persons[]` | body | `array<object>` | no | Contact people associated with the contact. |
| `contact_persons[].first_name` | body | `string` | no | First name of the contact person. |
| `contact_persons[].last_name` | body | `string` | no | Last name of the contact person. |
| `contact_persons[].email` | body | `string` | no | Email address of the contact person. |
