# xAI: Get TTS Voice

Retrieves a text-to-speech voice from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-tts-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-tts-voice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-tts-voice?${params}`, {
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
| `voice_id` | string | no | Voice identifier, such as eve or ara. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "name": "Ava Chen",
      "voice_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string |  |
| `name` | string |  |
| `voice_id` | string |  |

## Native endpoint

Through the native xAI API, this operation is `GET /tts/voices/:voice_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tts-voice.md) for the provider-specific parameters and requirements.

