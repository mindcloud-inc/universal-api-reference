# Query Deployment Logs with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/deployment_logs/query`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [Query Deployment Logs](https://docs.deepinfra.com/api-reference/logs-&-metrics/deployment-logs-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploy_id` | query | `string` | yes | Deployment ID whose deployment logs should be queried. |
