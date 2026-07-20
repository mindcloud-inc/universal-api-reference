# Update Contact with AMcards.com

Updates an existing contact in AMcards.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contact/:contactId/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [Update Contact](https://staging.amcards.com/docs/developers-only/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | no | AMcards contact identifier from the `/contact/` resource URI. |
| `email_address` | body | `string` | no | Updated email address for the contact. |
