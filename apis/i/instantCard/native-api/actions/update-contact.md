# Update Contact with InstantCard

Updates an existing contact in InstantCard.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/organizations/:organizationId/contacts/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Update Contact](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact[alt_email]` | query | `string` | no | Alternate email. |
| `contact[alt_phone_number]` | query | `string` | no | Alternate phone number. |
| `contact[email]` | query | `string` | no | Contact email. |
| `contact[full_name]` | query | `string` | no | Contact full name. |
| `contact[phone_number]` | query | `string` | no | Phone number. |
| `id` | path | `number` | yes | Contact ID from InstantCard. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
