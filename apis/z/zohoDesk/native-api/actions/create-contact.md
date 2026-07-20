# Create Contact with Zoho Desk

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Create Contact](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastName` | body | `string` | yes | Last name for the new contact. |
| `email` | body | `string` | no | Email for the new contact. |
