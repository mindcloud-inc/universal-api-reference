# Create Customer with Sponsy

Creates a customer in Sponsy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Create Customer](https://docs.getsponsy.com/CRM-182b5594716880bd9d7afde179bc1114)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Customer name. |
| `contact` | body | `object` | no | Primary customer contact. |
| `contact.firstName` | body | `string` | yes | Primary contact first name. |
| `contact.lastName` | body | `string` | yes | Primary contact last name. |
| `contact.email` | body | `string` | yes | Primary contact email. |
