# List Tickets with HubSpot

Retrieves tickets from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/tickets`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Tickets](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/basic/get-crm-v3-objects-tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | Ticket properties to return in the response. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Ticket properties to return with value history. |
| `associations[]` | query | `array<string>` | no | Associated object types to include as associated IDs. |
| `archived` | query | `boolean` | no | Whether to return archived ticket records. |
