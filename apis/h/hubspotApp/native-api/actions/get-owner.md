# Get Owner with HubSpot

Retrieves an owner from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/owners/:ownerId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Owner](https://developers.hubspot.com/docs/api-reference/crm-crm-owners-v3/owners/get-crm-v3-owners-ownerId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownerId` | path | `string` | yes | The identifier of the owner to retrieve. |
| `archived` | query | `boolean` | no | Whether to return archived owners. |
| `idProperty` | query | `string` | no | The identifier type for ownerId, such as the HubSpot owner id or the owner userId. |
