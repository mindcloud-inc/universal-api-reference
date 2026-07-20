# Get Deal by ID with HubSpot

Retrieves a deal from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/deals/:dealId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Deal by ID](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/get-crm-v3-objects-0-3-dealId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `string` | yes | The unique ID of the deal to retrieve. |
| `properties[]` | query | `array<string>` | no | Deal properties to return in the response. Send multiple values as a array. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Deal properties to return with value history. |
| `associations` | query | `string<string>` | no | Associated object types to include as associated IDs. Send multiple values as a array. |
| `archived` | query | `boolean` | no | Whether to return archived deal records. |
| `idProperty` | query | `string` | no | The unique property to use for dealId instead of the default record ID. |
