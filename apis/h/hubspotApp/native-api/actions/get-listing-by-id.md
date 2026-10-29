# Get Object Record by ID with HubSpot

Retrieves a listing from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/:objectTypeId/:objectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Object Record by ID](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts-contactId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectTypeId` | path | `string` | yes | The object type, for example contacts, companies, or a custom object type ID like 2-123456; also accepts the fully qualified name, like p123456_my_object. |
| `objectId` | path | `string` | yes | The ID of the record to read. |
| `properties[]` | query | `array<string>` | no | Internal property names to include in the response. |
