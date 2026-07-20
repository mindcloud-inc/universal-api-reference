# Find agents for customer with Atera

Finds agents in Atera for a specific customer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/agents/customer/:customerId`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Find agents for customer](https://app.atera.com/apidocs#!/Agent/Agent_GetByCustomer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | System customer ID. |
