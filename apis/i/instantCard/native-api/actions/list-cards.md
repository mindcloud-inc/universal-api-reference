# List Cards with InstantCard

Retrieves all organization cards from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/cards`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Cards](https://instantcard.net/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
