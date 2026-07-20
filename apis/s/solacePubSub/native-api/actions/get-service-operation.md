# Get Service Operation with Solace PubSub+

Retrieves a service operation from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/missionControl/eventBrokerServices/{serviceId}/operations/{operationId}`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get Service Operation](https://api.solace.dev/cloud/reference/getserviceoperation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | path | `string` | yes | Event broker service identifier. |
| `operationId` | path | `string` | yes | Service operation identifier. |
