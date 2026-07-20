# List Customers with Landbot

Retrieves customers from Landbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [List Customers](https://api.landbot.io/#api-Customers-GetHttpsApiLandbotIoV1Customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | query | `number` | no | Channel ID of the customers. |
| `agent_id` | query | `number` | no | Agent ID of the customers. |
| `search_by` | query | `string` | no | Field to search by. |
| `search` | query | `string` | no | Value to search; Landbot applies a starts-with match. |
| `archived` | query | `boolean` | no | Include archived customers. |
| `opt_in` | query | `boolean` | no | Filter by WhatsApp opt-in status. |
