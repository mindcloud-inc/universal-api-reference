# Beyond Presence: List Agents

Retrieves available agents from Beyond Presence.

```
GET https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-agents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Beyond Presence API, this operation is `GET /v1/agents` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

