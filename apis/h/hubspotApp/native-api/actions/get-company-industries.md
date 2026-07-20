# Get Company Industries with HubSpot

Retrieves the company industry property from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/properties/companies/industry`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Company Industries](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType-propertyName)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSensitivity` | query | `list<string>` | no | The data sensitivity filter to apply. |
| `locale` | query | `string` | no | The locale to use when returning property details. |
| `archived` | query | `boolean` | no | Whether to include archived property metadata. |
