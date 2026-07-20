# List Addresses with InstantCard

Retrieves all saved addresses from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/addresses`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Addresses](https://instantcard.net/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
