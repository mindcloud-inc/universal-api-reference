# Create Agent with Chatvolt AI

Creates an agent in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Agent](https://docs.chatvolt.ai/api-reference/endpoint/agents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Agent name. If not provided, a fun name will be generated automatically. |
| `description` | body | `string` | no | Agent description. |
| `modelName` | body | `string` | no | LLM model to be used by the agent. Check the API for [available model names](https://api.chatvolt.ai/agents/models). |
| `temperature` | body | `number` | no | Model temperature (min 0.0, max 1.0). Controls randomness. Model default if not specified. |
| `systemPrompt` | body | `string` | no | System prompt to guide the agent's behavior. |
| `visibility` | body | `string` | no | Agent visibility. `public` allows access without authentication (depending on other settings), `private` restricts access to the organization. |
| `handle` | body | `string` | no | A unique identifier (slug) for the agent. Used for friendly URLs. |
| `interfaceConfig` | body | `object` | no | Chat interface settings for this agent (colors, initial messages, etc.). |
| `configUrlExternal` | body | `object` | no | External URL configurations. |
| `configUrlInfosSystemExternal` | body | `object` | no | External URL configurations of the system. |
| `enableInactiveHours` | body | `boolean` | no | Enable or disable Inactive hours for the agent. |
| `inactiveHours` | body | `object` | no | A JSON object specifying the agent's inactive hours per channel. The top-level keys represent the channel (e.g., `whatsapp`, `website`,`instagram`), and each key contains an object with the days of the week and their respective inactive time ranges. |
| `tools[]` | body | `array<object>` | no | List of tools to be associated with the agent. |
