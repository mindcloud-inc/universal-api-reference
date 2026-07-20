# Run AI Task with OnceOnly

Runs an AI task in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/run`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Run AI Task](https://docs.onceonly.tech/reference/ai-run/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | no | Mode A background-run key. |
| `ttl` | body | `number` | no | Mode A lease duration in seconds. |
| `metadata` | body | `object` | no | Mode A metadata object. Can include run_id, agent_id, actions, and dry_run. |
| `agent_id` | body | `string` | no | Mode B agent id. |
| `tool` | body | `string` | no | Mode B governed tool name. |
| `args` | body | `object` | no | Mode B tool arguments object. |
| `spend_usd` | body | `number` | no | Optional spend estimate in USD. |
