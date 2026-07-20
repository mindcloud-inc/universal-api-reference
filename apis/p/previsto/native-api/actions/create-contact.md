# Create Contact with Previsto

Creates a new contact in Previsto.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Create Contact](https://developer.previsto.com/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Street address |
| `city` | body | `string` | no | City |
| `countryCode` | body | `string` | no | 2-letter country code |
| `name` | body | `string` | yes | Contact name. |
| `postalCode` | body | `string` | no | Postal code |
| `email` | body | `string` | no | Contact email. |
