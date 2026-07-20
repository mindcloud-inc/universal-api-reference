# Disconnect MQTT Client with MQTT

Disconnects an MQTT client from HiveMQ Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mqtt/clients/:clientId/connection`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Disconnect MQTT Client](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | MQTT client identifier whose connection should be disconnected. |
| `preventWillMessage` | query | `boolean` | no | When true, prevents the client will message from being sent during disconnection. |
