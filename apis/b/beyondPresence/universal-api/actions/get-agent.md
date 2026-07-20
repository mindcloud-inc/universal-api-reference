# Beyond Presence: Get Agent

Retrieves an agent from Beyond Presence.

```
GET https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-agent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-agent?${params}`, {
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
| `id` | string | yes | Agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarId": "string",
      "capabilities": [
        {}
      ],
      "greeting": "string",
      "id": "string",
      "knowledgeFileIds": [
        "string"
      ],
      "language": "string",
      "llm": {},
      "maxSessionLengthMinutes": 1,
      "name": "Ava Chen",
      "systemPrompt": "string",
      "tts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarId` | string | ID of the avatar used by the agent. |
| `capabilities` | array<object> | Additional capabilities configured for the agent. |
| `greeting` | string | Opening greeting used when a call starts. |
| `id` | string | Unique identifier of the agent. |
| `knowledgeFileIds` | array<string> | Knowledge file IDs attached to the agent. |
| `language` | string | Language configured for the agent. |
| `llm` | object | Language model configuration for the agent. |
| `maxSessionLengthMinutes` | number | Maximum session length in minutes. |
| `name` | string | Display name of the agent. |
| `systemPrompt` | string | System prompt configured for the agent. |
| `tts` | object | Text-to-speech configuration for the agent when present. |

## Native endpoint

Through the native Beyond Presence API, this operation is `GET /v1/agents/:id` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

