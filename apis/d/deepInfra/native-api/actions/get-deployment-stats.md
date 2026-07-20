# Get Deployment Stats with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/:deploy_id/stats`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [Get Deployment Stats](https://docs.deepinfra.com/api-reference/dedicated-models/deploy-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploy_id` | path | `string` | yes | Dedicated deployment identifier from the deployment stats URL path. |
| `from` | query | `string` | yes | Start of stats period as a Unix timestamp or relative value such as now-1h. |
