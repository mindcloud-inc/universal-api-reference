# List Organization Tickets with Deskpro

Retrieves tickets for an organization in Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/tickets`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [List Organization Tickets](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-organizations-{id}-tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
