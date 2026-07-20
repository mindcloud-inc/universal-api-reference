# Get Ticket by ID with HubSpot

Retrieves a ticket from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/tickets/:ticketId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Ticket by ID](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/basic/get-crm-v3-objects-tickets-ticketId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The unique ID of the ticket to retrieve. |
| `properties[]` | query | `array<string>` | no | Ticket properties to return in the response. |
| `properties[]WithHistory[]` | query | `array<string>` | no | Ticket properties to return with value history. |
| `associations[]` | query | `array<string>` | no | Associated object types to include as associated IDs. |
| `archived` | query | `boolean` | no | Whether to return archived ticket records. |
| `idProperty` | query | `string` | no | The unique property to use for ticketId instead of the default record ID. |
