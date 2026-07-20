# Get Email with HubSpot

Retrieves an email activity from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/emails/:emailId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Email](https://developers.hubspot.com/docs/api-reference/crm-emails-v3/basic/get-crm-v3-objects-emails-emailId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | The email record ID or unique property value when used with idProperty. |
| `properties[]` | query | `array<string>` | no | A list of properties to return. |
| `propertiesWithHistory[]` | query | `array<string>` | no | A list of properties to return with history. |
| `associations[]` | query | `array<string>` | no | A list of associated object types to retrieve. |
| `idProperty` | query | `string` | no | The name of a unique property to use instead of the record ID. |
| `archived` | query | `boolean` | no | Whether to include archived records. |
