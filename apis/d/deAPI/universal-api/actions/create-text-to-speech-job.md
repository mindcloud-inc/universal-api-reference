# deAPI: Create Text-to-Speech Job

Creates a text-to-speech job in deAPI.

```
POST https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-speech-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-speech-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-speech-job', {
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
| `format` | string | no | Audio output format such as mp3 or flac. |
| `lang` | string | no | Language code such as en-us. |
| `mode` | string | no | TTS mode. Use custom_voice for preset voices. |
| `model` | string | no | Speech model slug from List Models. |
| `sampleRate` | string | no | Sample rate for generated audio. |
| `speed` | string | no | Speech speed multiplier. |
| `text` | string | no | Text to convert to speech. |
| `voice` | string | no | Voice slug for custom_voice mode. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2audio` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-speech-job.md) for the provider-specific parameters and requirements.

