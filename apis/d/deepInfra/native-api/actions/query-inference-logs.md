# Query Inference Logs with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/logs/query`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [Query Inference Logs](https://docs.deepinfra.com/api-reference/logs-&-metrics/logs-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploy_id` | query | `string` | yes | Deployment ID whose inference logs should be queried. |
