# xAI: Create Text To Speech

Creates text-to-speech audio in the xAI API.

```
POST https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/create-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | Text to convert to speech. |
| `voice_id` | string | no | Voice identifier, such as eve or ara. |
| `language` | string | no | BCP-47 language code or auto. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio_bytes": 1,
      "content_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio_bytes` | number | Byte length when consumed by binary-aware clients. |
| `content_type` | string | Returned audio content type. |

## Native endpoint

Through the native xAI API, this operation is `POST /tts` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-speech.md) for the provider-specific parameters and requirements.

