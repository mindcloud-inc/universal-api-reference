# Search MQTT Clients with MQTT

Finds MQTT clients in HiveMQ Cloud by query parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/a/mqtt/clients/search`
- **Base URL:** `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`
- **Official documentation:** [Search MQTT Clients](https://docs.hivemq.com/hivemq-cloud/rest-api/specification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boolean-filter` | query | `string` | no | Boolean client search filter in the documented type:value format, for example CONNECTED:true. |
| `string-filter` | query | `string` | no | String client search filter in the documented type:operation:value format, for example ID:EQ:client1. |
| `number-filter` | query | `string` | no | Number client search filter in the documented type:operation:value format, for example MAX_QUEUE_SIZE:GT:100. |
| `limit` | query | `number` | no | Page size between 50 and 2500. HiveMQ documents 500 as the default. |
| `cursor` | query | `string` | no | Cursor returned by the previous search page. |
