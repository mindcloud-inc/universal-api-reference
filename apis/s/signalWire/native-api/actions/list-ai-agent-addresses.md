# List AI Agent Addresses with SignalWire

Retrieves AI agent addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/ai_agents/{ai_agent_id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List AI Agent Addresses](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/list-ai-agent-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ai_agent_id` | path | `string` | yes | Unique ID of a AI Agent. |
