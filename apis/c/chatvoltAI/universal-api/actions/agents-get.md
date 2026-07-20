# Chatvolt AI: Get Agent

Retrieves an agent from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Agent ID or its handle (unique identifier preceded by '@', e.g., '@my-agent'). |

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

Through the native Chatvolt AI API, this operation is `GET /agents/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-get.md) for the provider-specific parameters and requirements.

