# Get Broker State with Solace PubSub+

Retrieves broker state from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/missionControl/eventBrokerServices/{serviceId}/brokerState`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get Broker State](https://api.solace.dev/cloud/reference/getbrokerstatebyserviceid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | path | `string` | yes | Event broker service identifier. |
