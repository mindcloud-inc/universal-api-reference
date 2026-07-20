# Hamsa: Get Voice Agent By Id

Retrieves a voice agent from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-voice-agent-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-voice-agent-by-id?connectionId=$CONNECTION_ID&voiceAgentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voiceAgentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-voice-agent-by-id?${params}`, {
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
| `voiceAgentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "greetingMessage": "string",
      "id": "string",
      "lang": "string",
      "preamble": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentName` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `greetingMessage` | string |  |
| `id` | string |  |
| `lang` | string |  |
| `preamble` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/voice-agents/:voiceAgentId` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice-agent-by-id.md) for the provider-specific parameters and requirements.

