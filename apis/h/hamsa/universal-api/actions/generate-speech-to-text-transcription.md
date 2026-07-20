# Hamsa: Generate Speech to Text Transcription

Generates a speech-to-text transcription with Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-speech-to-text-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-speech-to-text-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/generate-speech-to-text-transcription', {
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
| `audioBase64` | string | no |  |
| `audioList[]` | array<number> | no | Accepts multiple values as an array. |
| `eosThreshold` | number | no | Default: `0.3`. |
| `isEosEnabled` | boolean | no | Default: `false`. |
| `language` | string | no | Default: `ar`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/realtime/stt` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-speech-to-text-transcription.md) for the provider-specific parameters and requirements.

