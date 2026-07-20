# Delete Client Contact with Timizer

Deletes an existing client contact from Timizer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/app/clients/:id/contacts/:contactId`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Delete Client Contact](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | ID of the contact. |
| `id` | path | `number` | yes | ID of the client. |
