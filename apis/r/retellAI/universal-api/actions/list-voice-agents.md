# Retell AI: List Voice Agents

Retrieves voice agents from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voice-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voice-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voice-agents?${params}`, {
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
| `paginationKeyVersion` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "agentName": "Ava Chen",
      "channel": "string",
      "dataStorageSetting": "string",
      "interruptionSensitivity": 1,
      "isPublished": true,
      "language": "string",
      "lastModificationTimestamp": 1,
      "maxCallDurationMs": 1,
      "postCallAnalysisData": [
        [
          {}
        ]
      ],
      "postCallAnalysisModel": "string",
      "responseEngine": {
        "conversationFlowId": "string",
        "llmId": "string",
        "type": "string",
        "version": 1
      },
      "userDtmfOptions": {},
      "version": 1,
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `agentName` | string |  |
| `channel` | string |  |
| `dataStorageSetting` | string |  |
| `interruptionSensitivity` | number |  |
| `isPublished` | boolean |  |
| `language` | string |  |
| `lastModificationTimestamp` | number |  |
| `maxCallDurationMs` | number |  |
| `postCallAnalysisData[]` | array<object> |  |
| `postCallAnalysisData[].choices[]` | array<string> |  |
| `postCallAnalysisData[].description` | string |  |
| `postCallAnalysisData[].name` | string |  |
| `postCallAnalysisData[].type` | string |  |
| `postCallAnalysisModel` | string |  |
| `responseEngine` | object |  |
| `responseEngine.conversationFlowId` | string |  |
| `responseEngine.llmId` | string |  |
| `responseEngine.type` | string |  |
| `responseEngine.version` | number |  |
| `userDtmfOptions` | object |  |
| `version` | number |  |
| `voiceId` | string |  |

## Native endpoint

Through the native Retell AI API, this operation is `GET /list-agents` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-voice-agents.md) for the provider-specific parameters and requirements.

