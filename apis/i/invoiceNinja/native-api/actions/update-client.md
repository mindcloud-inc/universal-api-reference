# Update Client with Invoice Ninja

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Client](https://api-docs.invoicing.co/#tag/clients/operation/updateClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hashed client ID from Invoice Ninja. |
| `name` | body | `string` | yes | Updated client company or organization name. |
| `country_id` | body | `number` | yes | Country identifier required by Invoice Ninja when updating a client. |
| `contacts[0].first_name` | body | `string` | yes | Primary contact first name. Invoice Ninja expects contacts to be sent on client updates. |
| `contacts[0].last_name` | body | `string` | yes | Primary contact last name. Invoice Ninja expects contacts to be sent on client updates. |
| `contacts[0].email` | body | `string` | yes | Primary contact email. Invoice Ninja expects contacts to be sent on client updates. |
| `public_notes` | body | `string` | no | Optional public notes shown on client-facing documents. |
