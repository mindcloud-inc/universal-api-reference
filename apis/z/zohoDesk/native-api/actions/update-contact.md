# Update Contact with Zoho Desk

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/[:contactId]`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Update Contact](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Zoho Desk contact ID. |
| `firstName` | body | `string` | no | Updated first name for the contact. |
