# Create Address with InstantCard

Creates a new address in InstantCard.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/addresses`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Create Address](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
| `address[organization_name]` | query | `string` | no | Organization name for the address. |
| `address[label]` | query | `string` | no | Address label. |
| `address[primary]` | query | `boolean` | no | Whether this is the primary address. |
| `address[address1]` | query | `string` | yes | Address line 1. |
| `address[address2]` | query | `string` | no | Address line 2. |
| `address[country]` | query | `string` | yes | Country. |
| `address[city]` | query | `string` | yes | City. |
| `address[state]` | query | `string` | yes | State or province code. |
| `address[zip_code]` | query | `string` | yes | Postal code. |
| `address[contact_id]` | query | `number` | no | Existing contact ID to link to this address. |
| `address[contact][full_name]` | query | `string` | yes | Full name for the linked contact. |
| `address[contact][email]` | query | `string` | yes | Email for the linked contact. |
| `address[contact][phone_number]` | query | `string` | no | Phone number for the linked contact. |
