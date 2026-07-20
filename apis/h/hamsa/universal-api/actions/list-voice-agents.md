# Hamsa: List Voice Agents

Retrieves voice agents from your Hamsa project.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-voice-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-voice-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-voice-agents?${params}`, {
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
| `language[]` | array<string> | no | Accepts multiple values as an array. Example: `ar,en`. |
| `search` | string | no | Example: `"Test Agent"`. |
| `skip` | number | no | Default: `1`. Example: `1`. |
| `sortField` | string | no | One of: `createdAt`. Example: `createdAt`. |
| `sortOrder` | string | no | One of: `asc`, `desc`. Example: `desc`. |
| `take` | number | no | Default: `10`. Example: `10`. |
| `type[]` | array<string> | no | Accepts multiple values as an array. Example: `Single Prompt,Flow Agent`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": {
        "greetingMessage": "string",
        "preamble": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "voice": {
        "lang": "string",
        "voiceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation.greetingMessage` | string |  |
| `conversation.preamble` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `voice.lang` | string |  |
| `voice.voiceId` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v2/voice-agents` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voice-agents.md) for the provider-specific parameters and requirements.

