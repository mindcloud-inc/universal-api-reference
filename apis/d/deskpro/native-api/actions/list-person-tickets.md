# List Person Tickets with Deskpro

Retrieves tickets for a person in Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/:personId/tickets`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Person Tickets](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-people-{id}-tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `personId` | path | `number` | yes |
