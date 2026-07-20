# Create or Update a Batch of Contacts with EZ Texting

Creates or updates multiple contacts in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/batch`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Create or Update a Batch of Contacts](https://developers.eztexting.com/reference/createorupdatebatch-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Contacts to create or update |
| `contacts[].phoneNumber` | body | `string` | no | Phone number |
| `contacts[].firstName` | body | `string` | no | First name |
| `contacts[].lastName` | body | `string` | no | Last name |
| `contacts[].email` | body | `string` | no | Email address |
| `contacts[].note` | body | `string` | no | Notes |
| `contacts[].custom1` | body | `string` | no | Custom value 1 |
| `contacts[].custom2` | body | `string` | no | Custom value 2 |
| `contacts[].custom3` | body | `string` | no | Custom value 3 |
| `contacts[].custom4` | body | `string` | no | Custom value 4 |
| `contacts[].custom5` | body | `string` | no | Custom value 5 |
| `contacts[].values` | body | `object` | no | — |
| `groupIdsAdd[]` | body | `array<string>` | no | Contact groups to add to each contact |
| `groupIdsRemove[]` | body | `array<string>` | no | Contact groups to remove from each contact |
