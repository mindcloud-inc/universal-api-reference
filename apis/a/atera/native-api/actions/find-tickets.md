# Find tickets with Atera

Finds tickets in Atera.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tickets`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find tickets](https://app.atera.com/apidocs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | query | `number` | no | Filter tickets by customer ID. |
| `ticketStatus` | query | `string` | no | Filter tickets by ticket status. |
| `includeRelations` | query | `boolean` | no | Include ticket relation information. |
