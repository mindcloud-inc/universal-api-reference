# Create or Update Contact with EZ Texting

Creates or updates a contact in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Create or Update Contact](https://developers.eztexting.com/reference/createorupdate-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom1` | body | `string` | no | Custom value 1 |
| `custom2` | body | `string` | no | Custom value 2 |
| `custom3` | body | `string` | no | Custom value 3 |
| `custom4` | body | `string` | no | Custom value 4 |
| `custom5` | body | `string` | no | Custom value 5 |
| `email` | body | `string` | no | Contact email address |
| `firstName` | body | `string` | no | Contact first name |
| `groupIdsAdd[]` | body | `array<string>` | no | Contact groups to add |
| `groupIdsRemove[]` | body | `array<string>` | no | Contact groups to remove |
| `lastName` | body | `string` | no | Contact last name |
| `note` | body | `string` | no | Contact note |
| `phoneNumber` | body | `string` | no | Contact phone number |
| `values` | body | `object` | no | Additional dynamic contact values |
