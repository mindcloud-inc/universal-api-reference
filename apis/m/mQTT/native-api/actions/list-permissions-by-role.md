# List Permissions By Role with MQTT

Retrieves permissions for an MQTT role in HiveMQ Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/mqtt/roles/:roleIdOrName/permissions`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [List Permissions By Role](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleIdOrName` | path | `string` | yes | Role id or role name |
