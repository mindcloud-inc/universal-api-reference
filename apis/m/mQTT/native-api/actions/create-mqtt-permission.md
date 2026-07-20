# Create MQTT Permission with MQTT

Creates a new MQTT permission in HiveMQ Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/mqtt/permissions`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Create MQTT Permission](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permission.description` | body | `string` | yes | Description for the new MQTT permission |
| `permission.name` | body | `string` | yes | Name for the new MQTT permission |
| `permission.publishAllowed` | body | `boolean` | yes | Whether publishing is allowed |
| `permission.qos0Allowed` | body | `boolean` | yes | Whether QoS 0 is allowed |
| `permission.qos1Allowed` | body | `boolean` | yes | Whether QoS 1 is allowed |
| `permission.qos2Allowed` | body | `boolean` | yes | Whether QoS 2 is allowed |
| `permission.retainedMsgsAllowed` | body | `boolean` | yes | Whether retained messages are allowed |
| `permission.subscribeAllowed` | body | `boolean` | yes | Whether subscribing is allowed |
| `permission.topic` | body | `string` | yes | MQTT topic filter for this permission |
