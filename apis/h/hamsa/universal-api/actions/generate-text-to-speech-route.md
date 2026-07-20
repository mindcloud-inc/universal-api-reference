# Hamsa: Generate Text to Speech Route

Generates text-to-speech output in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-text-to-speech-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-text-to-speech-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-text-to-speech-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voiceId": "string",
    "voiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes |  |
| `voiceId` | string | yes |  |
| `voiceId` | string | yes |  |
| `webhookAuth` | object | no |  |
| `webhookUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jobResponse": {
        "text": "string",
        "ttsMediaFile": "string"
      },
      "mediaUrl": "https://example.com",
      "model": "string",
      "status": "string",
      "title": "string",
      "totalCost": 1,
      "ttsVoiceId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `jobResponse.text` | string |  |
| `jobResponse.ttsMediaFile` | string |  |
| `mediaUrl` | string |  |
| `model` | string |  |
| `status` | string |  |
| `title` | string |  |
| `totalCost` | number |  |
| `ttsVoiceId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/jobs/text-to-speech` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-text-to-speech-route.md) for the provider-specific parameters and requirements.

