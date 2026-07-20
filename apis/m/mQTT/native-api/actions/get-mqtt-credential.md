# Get MQTT Credential with MQTT

Retrieves an MQTT credential from HiveMQ Cloud by username.

## Endpoint

- **Method:** `GET`
- **Path:** `/mqtt/credentials/username/:username`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Get MQTT Credential](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | MQTT credential username |
