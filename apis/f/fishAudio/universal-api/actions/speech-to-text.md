# Fish Audio: Speech to Text

Transcribes audio to text with Fish Audio.

```
POST https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/speech-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/speech-to-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/speech-to-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio` | file | yes | Audio file to transcribe. |
| `language` | string | no | Optional language hint. |
| `ignoreTimestamps` | boolean | no | When true, Fish Audio skips detailed timestamp output. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "segments": [
        {}
      ],
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `segments` | array<object> |  |
| `text` | string |  |

## Native endpoint

Through the native Fish Audio API, this operation is `POST /v1/asr` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/speech-to-text.md) for the provider-specific parameters and requirements.

