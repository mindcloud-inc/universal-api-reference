# List Agent Result Logs with Release0

Retrieves execution logs for a Release0 agent result.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agentId/results/:resultId/logs`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [List Agent Result Logs](https://docs.release0.com/submission/realtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID. |
| `resultId` | path | `string` | yes | The result ID. |
