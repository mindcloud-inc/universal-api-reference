# Update Contact with Previsto

Updates an existing contact in Previsto.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Update Contact](https://developer.previsto.com/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Street address |
| `city` | body | `string` | no | City |
| `countryCode` | body | `string` | no | 2-letter country code |
| `id` | path | `string` | yes | Previsto contact ID. |
| `postalCode` | body | `string` | no | Postal code |
| `name` | body | `string` | no | Updated contact name. |
| `email` | body | `string` | no | Updated contact email. |
