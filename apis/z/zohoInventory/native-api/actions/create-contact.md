# Create Contact with Zoho Inventory

Creates a new contact in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Create Contact](https://www.zoho.com/inventory/api/v1/contacts/#create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `contact_name` | body | `string` | yes | The display name for the contact. |
| `contact_type` | body | `string` | no | Whether the contact is a customer or vendor. |
| `company_name` | body | `string` | no | Company name for a business contact. |
| `notes` | body | `string` | no | Internal notes for the contact. |
| `contact_persons[]` | body | `array<object>` | no | One or more contact people associated with this contact. |
| `contact_persons[].first_name` | body | `string` | no | First name of the contact person. |
| `contact_persons[].last_name` | body | `string` | no | Last name of the contact person. |
| `contact_persons[].email` | body | `string` | no | Email address for the contact person. |
| `contact_persons[].phone` | body | `string` | no | Phone number for the contact person. |
| `contact_persons[].is_primary_contact` | body | `boolean` | no | Whether this is the primary contact person. |
