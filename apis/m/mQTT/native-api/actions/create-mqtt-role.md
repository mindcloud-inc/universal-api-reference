# Create MQTT Role with MQTT

Creates a new MQTT role in HiveMQ Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/mqtt/roles`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Create MQTT Role](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role.description` | body | `string` | no | Description for the new MQTT role |
| `role.name` | body | `string` | yes | Name for the new MQTT role |
