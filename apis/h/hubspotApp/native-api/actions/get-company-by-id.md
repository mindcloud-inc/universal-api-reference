# Get Company by ID with HubSpot

Retrieves a company from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/companies/:companyId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Company by ID](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/get-crm-v3-objects-companies-companyId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | The company record ID. |
| `properties[]` | query | `array<string>` | no | Company properties to return in the response. Send multiple values as a string separated by `,`. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Company properties to return with value history. Send multiple values as a string separated by `,`. |
| `associations[]` | query | `array<string>` | no | Associated object types to include as associated IDs. Send multiple values as a string separated by `,`. |
| `archived` | query | `boolean` | no | Whether to return archived companies. |
