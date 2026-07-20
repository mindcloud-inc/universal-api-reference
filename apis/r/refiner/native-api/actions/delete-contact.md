# Delete Contact with Refiner

Deletes a contact from Refiner by ID or email.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Delete Contact](https://refiner.io/docs/api/#delete-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Delete the contact using your own user ID. |
| `email` | query | `string` | no | Delete the contact by email address. |
| `uuid` | query | `string` | no | Delete the contact by the Refiner UUID. |
