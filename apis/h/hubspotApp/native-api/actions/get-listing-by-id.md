# Get Listing By ID with HubSpot

Retrieves a listing from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/:objectTypeId/:objectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Listing By ID](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts-contactId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectTypeId` | path | `string` | yes | The Object Type ID. |
| `objectId` | path | `string` | yes | — |
| `properties[]` | query | `array<string>` | no | — |
