# Update Customer with Sponsy

Updates a customer in Sponsy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/customers/:customerId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Update Customer](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list<string>` | yes | Customer ID from List Customers. |
| `name` | body | `string` | yes | Customer name. |
| `contact` | body | `object` | no | Primary customer contact. |
| `contact.firstName` | body | `string` | yes | Primary contact first name. |
| `contact.lastName` | body | `string` | yes | Primary contact last name. |
| `contact.email` | body | `string` | yes | Primary contact email. |
