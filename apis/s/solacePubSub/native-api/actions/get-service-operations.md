# Get Service Operations with Solace PubSub+

Retrieves service operations from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/missionControl/eventBrokerServices/{serviceId}/operations`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get Service Operations](https://api.solace.dev/cloud/reference/getserviceoperations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | path | `string` | yes | Event broker service identifier. |
