# Detach Role From Credential with MQTT

Updates an MQTT credential in HiveMQ Cloud by detaching a role.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/:username/roles/:roleId/detach`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Detach Role From Credential](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `number` | yes | Numeric role identifier |
| `username` | path | `string` | yes | MQTT credential username |
