# List Credential Roles with MQTT

Retrieves roles for an MQTT credential in HiveMQ Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:username/roles`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [List Credential Roles](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | MQTT credential username |
