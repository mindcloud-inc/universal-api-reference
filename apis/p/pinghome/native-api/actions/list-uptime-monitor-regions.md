# List Uptime Monitor Regions with Pinghome

Retrieves uptime monitor regions from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/resource-query/v1/resource/:id/regions`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Uptime Monitor Regions](https://docs.pinghome.io/monitoring/uptime-monitoring/get-uptime-monitor-regions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the uptime monitor. |
