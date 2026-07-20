# Update Contact with Sakari SMS

Updates an existing contact in Sakari SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/:accountId/contacts/:contactId`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Update Contact](https://developer.sakari.io/api-reference/contacts/updates-a-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `mobile` | body | `object` | no |
| `mobile.number` | body | `string` | no |
| `mobile.country` | body | `string` | no |
