# Get Organization Balance with InstantCard

Retrieves an organization's current balance from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/balance`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Organization Balance](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
