# Get Address with InstantCard

Retrieves an address from InstantCard by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/addresses/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Address](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Address ID from InstantCard. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
