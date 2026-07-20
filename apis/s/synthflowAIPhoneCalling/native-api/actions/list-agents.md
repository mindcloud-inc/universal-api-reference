# List Agents with Synthflow AI Phone Calling

Retrieves all voice agents from Synthflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/assistants`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [List Agents](https://docs.synthflow.ai/api-reference/platform-api/agents/list-assistant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Agents displayed per page. |
| `offset` | query | `number` | no | Index of the first agent to return. |
