# Invalidate MQTT Client Session with MQTT

Invalidates an MQTT client session in HiveMQ Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mqtt/clients/:clientId`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Invalidate MQTT Client Session](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | MQTT client identifier whose session should be invalidated. |
| `preventWillMessage` | query | `boolean` | no | When true, prevents the client will message from being sent during invalidation. |
