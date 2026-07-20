# Get Contact with Refiner

Retrieves a contact from Refiner by ID or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Get Contact](https://refiner.io/docs/api/#get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Look up the contact by your own user ID. |
| `email` | query | `string` | no | Look up the contact by email address. |
| `uuid` | query | `string` | no | Look up the contact by the Refiner UUID. |
