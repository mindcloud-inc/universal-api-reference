# Update Contact with Omnisend

Updates an existing contact in Omnisend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v5/contacts/:contactID`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Update Contact](https://api-docs.omnisend.com/reference/patch_contacts-contactid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | — |
| `contactID` | path | `string` | yes | Unique Omnisend contact identifier. |
| `customProperties` | body | `object` | no | — |
| `identifiers[]` | body | `array<object>` | no | — |
| `identifiers[].channels` | body | `object` | no | — |
| `identifiers[].channels.email` | body | `object` | no | — |
| `identifiers[].channels.email.status` | body | `string` | no | — |
| `identifiers[].id` | body | `string` | no | — |
