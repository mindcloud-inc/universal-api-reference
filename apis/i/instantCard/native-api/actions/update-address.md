# Update Address with InstantCard

Updates an existing address in InstantCard.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/organizations/:organizationId/addresses/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Update Address](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address[address1]` | query | `string` | no | Address line 1. |
| `address[address2]` | query | `string` | no | Address line 2. |
| `address[city]` | query | `string` | no | City. |
| `address[contact][email]` | query | `string` | no | Email for the linked contact. |
| `address[contact][full_name]` | query | `string` | no | Full name for the linked contact. |
| `address[contact][phone_number]` | query | `string` | no | Phone number for the linked contact. |
| `address[country]` | query | `string` | no | Country. |
| `address[label]` | query | `string` | no | Address label. |
| `address[organization_name]` | query | `string` | no | Organization name for the address. |
| `address[zip_code]` | query | `string` | no | Postal code. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
| `id` | path | `number` | yes | Address ID from InstantCard. |
| `address[contact_id]` | query | `number` | no | Existing contact ID to link to this address. |
| `address[primary]` | query | `boolean` | no | Whether this is the primary address. |
| `address[state]` | query | `string` | no | State or province code. |
