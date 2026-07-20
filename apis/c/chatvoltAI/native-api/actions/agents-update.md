# Update Agent with Chatvolt AI

Updates an agent in Chatvolt AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Agent](https://docs.chatvolt.ai/api-reference/endpoint/agents/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the agent to be updated. |
| `name` | body | `string` | no | New name for the agent. |
| `description` | body | `string` | no | New description for the agent. |
| `modelName` | body | `string` | no | New LLM model to be used by the agent. Check the API for [available model names](https://api.chatvolt.ai/agents/models). |
| `temperature` | body | `number` | no | New model temperature (min 0.0, max 1.0). |
| `systemPrompt` | body | `string` | no | New system prompt for the agent. |
| `visibility` | body | `string` | no | New visibility for the agent. |
| `handle` | body | `string` | no | New unique identifier (slug) for the agent. |
| `interfaceConfig` | body | `object` | no | New chat interface settings for this agent. Replaces the existing object. |
| `enableInactiveHours` | body | `boolean` | no | Enable or disable Inactive hours for the agent. |
| `inactiveHours` | body | `object` | no | A JSON object specifying the agent's inactive hours per channel. The top-level keys represent the channel (e.g., `whatsapp`, `website`,`instagram`), and each key contains an object with the days of the week and their respective inactive time ranges. |
| `configUrlExternal` | body | `object` | no | New external URL configurations. Replaces the existing object. |
| `configUrlInfosSystemExternal` | body | `object` | no | New external URL configurations of the system. Replaces the existing object. |
| `tools[]` | body | `array<object>` | no | List of tools for the agent. This array defines the final state of the tools. - Tools in the array **without** an `id` will be **created**. - Tools in the array **with** an existing `id` will be **updated** (only `config` is updatable for `http`, `form`, `lead_capture` types). - Existing tools in the agent that are **not** present in this array will be **removed**. |
