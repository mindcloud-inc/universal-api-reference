# Invoke Agent with Agent.ai

Invokes an agent in Agent.ai with input or a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/invoke_agent`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Invoke Agent](https://docs.agent.ai/api-reference/advanced/invoke-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Agent ID or human-readable slug. |
| `user_input` | body | `string` | yes | Prompt or input text for the agent. |
| `run_id` | body | `string` | no | Optional run identifier for resuming a knowledge-agent conversation. |
