# Create or Update a Contact List with Chatvolt AI

Creates a contact list in Chatvolt AI, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/dispatches/contacts/lists`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create or Update a Contact List](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Include the ID to update an existing contact list. Omit to create a new one. |
| `name` | body | `string` | no | The name of the contact list. |
