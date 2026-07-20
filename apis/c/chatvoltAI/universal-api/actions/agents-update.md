# Chatvolt AI: Update Agent

Updates an agent in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the agent to be updated. |
| `name` | string | no | New name for the agent. |
| `description` | string | no | New description for the agent. |
| `modelName` | string | no | New LLM model to be used by the agent. Check the API for [available model names](https://api.chatvolt.ai/agents/models). |
| `temperature` | number | no | New model temperature (min 0.0, max 1.0). |
| `systemPrompt` | string | no | New system prompt for the agent. |
| `visibility` | string | no | New visibility for the agent. |
| `handle` | string | no | New unique identifier (slug) for the agent. |
| `interfaceConfig` | object | no | New chat interface settings for this agent. Replaces the existing object. |
| `enableInactiveHours` | boolean | no | Enable or disable Inactive hours for the agent. |
| `inactiveHours` | object | no | A JSON object specifying the agent's inactive hours per channel. The top-level keys represent the channel (e.g., `whatsapp`, `website`,`instagram`), and each key contains an object with the days of the week and their respective inactive time ranges. |
| `configUrlExternal` | object | no | New external URL configurations. Replaces the existing object. |
| `configUrlInfosSystemExternal` | object | no | New external URL configurations of the system. Replaces the existing object. |
| `tools[]` | array<object> | no | List of tools for the agent. This array defines the final state of the tools. - Tools in the array **without** an `id` will be **created**. - Tools in the array **with** an existing `id` will be **updated** (only `config` is updatable for `http`, `form`, `lead_capture` types). - Existing tools in the agent that are **not** present in this array will be **removed**. |

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

Through the native Chatvolt AI API, this operation is `PATCH /agents/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-update.md) for the provider-specific parameters and requirements.

