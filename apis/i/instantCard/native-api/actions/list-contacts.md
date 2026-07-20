# List Contacts with InstantCard

Retrieves all organization contacts from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/contacts`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Contacts](https://instantcard.net/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
