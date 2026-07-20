# List Associations with HubSpot

Retrieves associations for a HubSpot record.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v4/objects/:fromObject/:objectId/associations/:toObjectType`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Associations](https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromObject` | path | `string` | yes | The source object type. |
| `objectId` | path | `string` | yes | The source record ID. |
| `toObjectType` | path | `string` | yes | The associated target object type. |
