# List Owners with HubSpot

Retrieves owners from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/owners/`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Owners](https://developers.hubspot.com/docs/api-reference/crm-crm-owners-v3/owners/get-crm-v3-owners-)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | The email address of the owner to return. |
| `archived` | query | `boolean` | no | Whether to return archived owners. |
