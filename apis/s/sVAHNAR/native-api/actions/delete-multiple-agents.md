# Delete Multiple Agents with SVAHNAR

Deletes multiple agents from SVAHNAR.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/agents/bulk-delete`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Delete Multiple Agents](https://docs.svahnar.com/docs/Agents/delete_agent/#delete-multiple-agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_ids[]` | body | `array<string>` | yes | The list of agent IDs to delete. |
