# Get Agent Metrics with OnceOnly

Retrieves agent metrics from OnceOnly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/metrics`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Get Agent Metrics](https://docs.onceonly.tech/reference/agents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | Agent id to inspect. |
| `period` | query | `string` | no | Aggregation period: hour, day, or week. |
