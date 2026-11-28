# Create Contact with MoneyBird

Creates a new contact in MoneyBird.

## Endpoint

- **Method:** `POST`
- **Path:** `/:administrationId/contacts.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Create Contact](https://developer.moneybird.com/api/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `contact` | body | `object` | no | — |
| `contact.company_name` | body | `string` | no | — |
| `contact.firstname` | body | `string` | no | — |
| `contact.lastname` | body | `string` | no | — |
| `contact.email` | body | `string` | no | — |
| `contact.phone` | body | `string` | no | — |
| `contact.address1` | body | `string` | no | — |
| `contact.address2` | body | `string` | no | — |
| `contact.zipcode` | body | `string` | no | — |
| `contact.city` | body | `string` | no | — |
| `contact.country` | body | `string` | no | — |
| `contact.customer_id` | body | `string` | no | — |
