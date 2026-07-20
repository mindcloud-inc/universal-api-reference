# List MQTT Client Subscriptions with MQTT

Retrieves subscriptions for an MQTT client in HiveMQ Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/mqtt/clients/:clientId/subscriptions`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [List MQTT Client Subscriptions](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | MQTT client identifier |
