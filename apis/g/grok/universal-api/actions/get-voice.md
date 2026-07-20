# Grok: Get Voice

Retrieves a specific voice from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-voice?connectionId=$CONNECTION_ID&voiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-voice?${params}`, {
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
| `voiceId` | string | yes | Voice identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "name": "Ava Chen",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string | Supported language for the voice. |
| `name` | string | Display name for the voice. |
| `voiceId` | string | Voice identifier. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/tts/voices/:voice_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice.md) for the provider-specific parameters and requirements.

