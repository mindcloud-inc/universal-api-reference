# List Agent Logs with OnceOnly

Retrieves agent logs from OnceOnly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/logs`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [List Agent Logs](https://docs.onceonly.tech/reference/agents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | Agent id to inspect. |
| `limit` | query | `number` | no | Results per page. |
