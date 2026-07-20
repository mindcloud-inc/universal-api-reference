# Chatvolt AI: Create Agent

Creates an agent in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Agent name. If not provided, a fun name will be generated automatically. |
| `description` | string | no | Agent description. |
| `modelName` | string | no | LLM model to be used by the agent. Check the API for [available model names](https://api.chatvolt.ai/agents/models). |
| `temperature` | number | no | Model temperature (min 0.0, max 1.0). Controls randomness. Model default if not specified. |
| `systemPrompt` | string | no | System prompt to guide the agent's behavior. |
| `visibility` | string | no | Agent visibility. `public` allows access without authentication (depending on other settings), `private` restricts access to the organization. |
| `handle` | string | no | A unique identifier (slug) for the agent. Used for friendly URLs. |
| `interfaceConfig` | object | no | Chat interface settings for this agent (colors, initial messages, etc.). |
| `configUrlExternal` | object | no | External URL configurations. |
| `configUrlInfosSystemExternal` | object | no | External URL configurations of the system. |
| `enableInactiveHours` | boolean | no | Enable or disable Inactive hours for the agent. |
| `inactiveHours` | object | no | A JSON object specifying the agent's inactive hours per channel. The top-level keys represent the channel (e.g., `whatsapp`, `website`,`instagram`), and each key contains an object with the days of the week and their respective inactive time ranges. |
| `tools[]` | array<object> | no | List of tools to be associated with the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configUrlExternal": {},
      "configUrlInfosSystemExternal": {},
      "createdAt": "string",
      "description": "string",
      "enableInactiveHours": true,
      "handle": "string",
      "id": "string",
      "inactiveHours": {},
      "interfaceConfig": {},
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "systemPrompt": "string",
      "temperature": 1,
      "tools": [
        "string"
      ],
      "updatedAt": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configUrlExternal` | object | External URL configurations. |
| `configUrlInfosSystemExternal` | object | External URL configurations of the system. |
| `createdAt` | string | Timestamp of when the agent was created. |
| `description` | string | Description. |
| `enableInactiveHours` | boolean | Enable or disable Inactive hours for the agent. |
| `handle` | string | A unique identifier (slug) for the agent. |
| `id` | string | Id. |
| `inactiveHours` | object | A JSON object specifying the agent's inactive hours per channel. The top-level keys represent the channel (e.g., `whatsapp`, `website`,`instagram`), and each key contains an object with the days of the week and their respective inactive time ranges. |
| `interfaceConfig` | object | Chat interface settings for this agent. |
| `modelName` | string | LLM - Model name. |
| `name` | string | Name. |
| `organizationId` | string | ID of the organization the agent belongs to. |
| `systemPrompt` | string | Agent system prompt |
| `temperature` | number | Temperature of the model (min 0.0, max 1.0) |
| `tools` | array | List of tools associated with the agent. |
| `updatedAt` | string | Timestamp of the last update to the agent. |
| `visibility` | string | Visibility. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /agents` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-create.md) for the provider-specific parameters and requirements.

