# List Custom Object Records with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/:objectTypeId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Custom Object Records](https://developers.hubspot.com/docs/api-reference/legacy/crm/objects/custom-objects/guide)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectTypeId` | path | `string` | yes | The custom object type ID from this HubSpot account, such as 2-123456. Use the object type ID, not its display label or a record ID. |
| `properties` | query | `string<string>` | no | Comma-separated internal property names to include in each record. Include the fields needed by your report. |
| `propertiesWithHistory` | query | `string<string>` | no | Comma-separated internal property names to return with their current and historical values. |
| `associations` | query | `string<string>` | no | Comma-separated object types whose associated record IDs should be included. |
