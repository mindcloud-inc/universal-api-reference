# Create Customer Contact with ServiceTitan

Creates a new customer contact in ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v2/tenant/{tenant}/customers/:id/contacts`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Customer Contact](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_CreateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | — |
| `type` | body | `string` | yes | Phone, MobilePhone, Email, or Fax |
| `value` | body | `string` | yes | The email, phone number, or fax number for the contact |
| `memo` | body | `string` | no | Short description about this contact, for example, “work #” or “Owner’s daughter - Kelly” |
