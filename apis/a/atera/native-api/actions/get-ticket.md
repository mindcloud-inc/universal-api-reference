# Get ticket with Atera

Retrieves a ticket from Atera by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tickets/:ticketId`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Get ticket](https://app.atera.com/apidocs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `number` | yes | System ticket ID. |
| `includeRelations` | query | `boolean` | no | Include ticket relation information. |
