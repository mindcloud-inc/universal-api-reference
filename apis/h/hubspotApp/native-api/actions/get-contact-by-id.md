# Get Contact by ID with HubSpot

Retrieves a contact from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/contacts/:contactId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Contact by ID](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts-contactId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The contact record ID. |
| `properties[]` | query | `array<string>` | no | Contact properties to return in the response. Send multiple values as a string separated by `,`. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Contact properties to return with value history. Send multiple values as a string separated by `,`. |
| `associations[]` | query | `array<string>` | no | Associated object types to include as associated IDs. Send multiple values as a string separated by `,`. |
| `archived` | query | `boolean` | no | Whether to return archived contacts. |
