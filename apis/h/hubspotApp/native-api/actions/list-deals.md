# List Deals with HubSpot

Retrieves deals from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/deals`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Deals](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/get-crm-v3-objects-0-3)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | Deal properties to return in the response. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Deal properties to return with value history. |
| `associations` | query | `string<string>` | no | Associated object types to include as associated IDs. Send multiple values as a array. |
| `archived` | query | `boolean` | no | Whether to return archived deal records. |
