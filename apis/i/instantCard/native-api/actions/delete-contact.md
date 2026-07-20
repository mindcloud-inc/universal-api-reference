# Delete Contact with InstantCard

Deletes an existing contact from InstantCard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/organizations/:organizationId/contacts/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Delete Contact](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact ID from InstantCard. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
