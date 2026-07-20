# Create Contact with Trust

Creates a new contact in Trust.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.usetrust.app/v1`
- **Official documentation:** [Create Contact](https://api-docs.usetrust.io/api-reference-swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address of contact. |
| `firstname` | body | `string` | no | First name of contact. |
| `imageUrl` | body | `string` | no | URL to the contact image. |
| `lastname` | body | `string` | no | Last name of contact. |
| `phone` | body | `string` | no | Phone number of the contact. |
| `workspaceId` | body | `string` | yes | The Trust workspace id (typeId). |
