# Create Contact with InstantCard

Creates a new contact in InstantCard.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/contacts`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Create Contact](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact[alt_email]` | query | `string` | no | Alternate email. |
| `contact[alt_phone_number]` | query | `string` | no | Alternate phone number. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
| `contact[full_name]` | query | `string` | yes | Contact full name. |
| `contact[email]` | query | `string` | yes | Contact email. |
| `contact[phone_number]` | query | `string` | no | Phone number. |
