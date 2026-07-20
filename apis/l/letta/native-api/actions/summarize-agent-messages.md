# Summarize Agent Messages with Letta

Summarizes an agent's conversation history in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agent_id/summarize`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Summarize Agent Messages](https://docs.letta.com/api/resources/agents/subresources/messages/methods/compact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `compaction_settings` | body | `object` | no | Optional Letta compaction settings. Use mode all when summarizing short test conversations. |
