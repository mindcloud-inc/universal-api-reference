# Attach Permission To Role with MQTT

Updates an MQTT role in HiveMQ Cloud by attaching a permission.

## Endpoint

- **Method:** `PUT`
- **Path:** `/mqtt/roles/:roleId/permissions/:permissionId/attach`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Attach Permission To Role](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permissionId` | path | `number` | yes | Numeric permission identifier |
| `roleId` | path | `number` | yes | Numeric role identifier |
