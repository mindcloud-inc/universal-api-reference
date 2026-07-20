# Edit Contact List with Chatvolt AI

Updates an existing contact list in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dispatches/contacts/lists`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Edit Contact List](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Include the ID to update an existing contact list. Omit to create a new one. |
| `name` | body | `string` | no | The name of the contact list. |
