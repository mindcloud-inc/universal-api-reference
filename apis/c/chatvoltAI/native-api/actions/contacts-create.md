# Create or Update Contact with Chatvolt AI

Creates a contact in Chatvolt AI, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create or Update Contact](https://docs.chatvolt.ai/api-reference/endpoint/contacts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Include the ID to update an existing contact. Omit to create a new one. |
| `email` | body | `string` | no | Email for application/json requests. |
| `phoneNumber` | body | `string` | no | PhoneNumber for application/json requests. |
| `firstName` | body | `string` | no | FirstName for application/json requests. |
| `lastName` | body | `string` | no | LastName for application/json requests. |
| `externalId` | body | `string` | no | ExternalId for application/json requests. |
| `picture` | body | `string` | no | Picture for application/json requests. |
| `metadata` | body | `object` | no | Metadata for application/json requests. |
