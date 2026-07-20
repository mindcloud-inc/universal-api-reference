# List Contacts with HubSpot

Retrieves contacts from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/contacts`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Contacts](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | Contact properties to return in the response. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Contact properties to return with value history. |
| `associations[]` | query | `array<string>` | no | Associated object types to include as associated IDs. |
| `archived` | query | `boolean` | no | Whether to return only archived contact records. |
