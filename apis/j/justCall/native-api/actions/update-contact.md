# Update Contact with JustCall

Updates an existing contact in JustCall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2.1/contacts`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Update Contact](https://developer.justcall.io/reference/update_contact_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Updated company name for the contact. |
| `id` | body | `number` | no | The JustCall contact ID to update. |
