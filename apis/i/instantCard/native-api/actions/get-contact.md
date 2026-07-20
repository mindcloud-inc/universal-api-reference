# Get Contact with InstantCard

Retrieves a contact from InstantCard by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/contacts/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Contact](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact ID from InstantCard. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
