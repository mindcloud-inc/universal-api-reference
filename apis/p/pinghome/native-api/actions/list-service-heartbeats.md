# List Service Heartbeats with Pinghome

Retrieves service heartbeats from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/resource-query/v1/service/:id/heartbeats`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Service Heartbeats](https://docs.pinghome.io/monitoring/heartbeat-monitoring/get-service-heartbeats/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the service. |
| `page` | query | `number` | no | The page number to retrieve. |
| `limit` | query | `number` | no | The maximum number of heartbeats to return. |
