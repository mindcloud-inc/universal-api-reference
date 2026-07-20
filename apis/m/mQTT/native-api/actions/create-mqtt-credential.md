# Create MQTT Credential with MQTT

Creates a new MQTT credential in HiveMQ Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/mqtt/credentials`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Create MQTT Credential](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentials.password` | body | `string` | yes | Password for the new MQTT credential |
| `credentials.username` | body | `string` | yes | Username for the new MQTT credential |
