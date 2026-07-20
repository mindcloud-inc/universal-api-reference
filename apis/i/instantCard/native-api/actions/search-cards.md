# Search Cards with InstantCard

Finds cards in InstantCard by search terms.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/cards/search`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Search Cards](https://instantcard.net/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `term` | query | `string` | yes | Single string used to search cards. |
