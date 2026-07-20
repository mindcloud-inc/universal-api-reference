# Ringg AI: Get Assistant By ID

Retrieves an assistant from Ringg AI by ID.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-by-id?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-by-id?${params}`, {
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
| `agentId` | string | yes | (Required) ID of the assistant to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents": {
        "agentConfig": {},
        "agentDisplayName": "Ava Chen",
        "agentType": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "formFields": [
          {
            "key": "string",
            "value": "string"
          }
        ],
        "id": "string",
        "knowledgeBaseId": "string",
        "knowledgeBaseName": "Ava Chen",
        "language": "string",
        "secondaryLanguage": "string",
        "secondaryVoiceId": "string",
        "templateIcon": "string",
        "templateLabel": "string",
        "templateName": "Ava Chen",
        "templateType": "string",
        "tools": [
          {
            "config": {},
            "name": "Ava Chen",
            "toolType": "string"
          }
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "voice": {
          "id": "string",
          "name": "Ava Chen",
          "voicePreview": "string"
        },
        "whitelistedDomains": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | object |  |
| `agents.agentConfig` | object |  |
| `agents.agentDisplayName` | string |  |
| `agents.agentType` | string |  |
| `agents.createdAt` | date |  |
| `agents.formFields` | array<object> |  |
| `agents.formFields[].key` | string |  |
| `agents.formFields[].value` | string |  |
| `agents.id` | string |  |
| `agents.knowledgeBaseId` | string |  |
| `agents.knowledgeBaseName` | string |  |
| `agents.language` | string |  |
| `agents.secondaryLanguage` | string |  |
| `agents.secondaryVoiceId` | string |  |
| `agents.templateIcon` | string |  |
| `agents.templateLabel` | string |  |
| `agents.templateName` | string |  |
| `agents.templateType` | string |  |
| `agents.tools` | array<object> |  |
| `agents.tools[].config` | object |  |
| `agents.tools[].name` | string |  |
| `agents.tools[].toolType` | string |  |
| `agents.updatedAt` | date |  |
| `agents.voice` | object |  |
| `agents.voice.id` | string |  |
| `agents.voice.name` | string |  |
| `agents.voice.voicePreview` | string |  |
| `agents.whitelistedDomains` | array<string> |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /agent/:agent_id` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assistant-by-id.md) for the provider-specific parameters and requirements.

