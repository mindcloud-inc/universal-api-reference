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
| `properties` | query | `list<string>` | no | Contact properties to return in the response. Select properties from the lookup when available; HubSpot requires internal property names. Common labels such as Lead Source and lifecycle-stage date-entered labels are normalized automatically. Send multiple values as a string separated by `,`. |
| `propertiesWithHistory` | query | `list<string>` | no | Contact properties to return with value history. Select properties from the lookup when available; HubSpot requires internal property names. Common labels such as Lead Source and lifecycle-stage date-entered labels are normalized automatically. Send multiple values as a string separated by `,`. |
| `associations` | query | `string<string>` | no | Associated object types to include as associated IDs. Send multiple values as a string separated by `,`. |
| `archived` | query | `boolean` | no | Whether to return only archived contact records. |
