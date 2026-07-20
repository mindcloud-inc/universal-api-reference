# Create Contact with Microsoft 365 People

Creates a new contact in Microsoft 365 People.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/contacts`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Contact](https://learn.microsoft.com/en-us/graph/api/user-post-contacts?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | Display name for the new contact. |
| `givenName` | body | `string` | no | Given name for the new contact. |
| `surname` | body | `string` | no | Surname for the new contact. |
| `emailAddresses[].name` | body | `string` | no | Display name for the primary email address. |
| `emailAddresses[].address` | body | `string` | no | Primary email address for the contact. |
| `companyName` | body | `string` | no | Company name for the contact. |
| `jobTitle` | body | `string` | no | Job title for the contact. |
| `mobilePhone` | body | `string` | no | Mobile phone number for the contact. |
