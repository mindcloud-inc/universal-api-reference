# Get Contact with Zoho Inventory

Retrieves a contact from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Contact](https://www.zoho.com/inventory/api/v1/contacts/#get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The Zoho Inventory contact_id for the contact. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
