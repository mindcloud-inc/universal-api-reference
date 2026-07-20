# TypeCast: Streaming Text To Speech

Creates streaming speech audio in TypeCast.

```
POST https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/streaming-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TypeCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/streaming-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string",
  "text": "string",
  "model": "ssfm-v21"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/streaming-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string",
    "text": "string",
    "model": "ssfm-v21"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | list | yes | TypeCast voice identifier to synthesize with. |
| `text` | string | yes | Text to convert to speech. |
| `model` | list | yes | TTS model version to use. One of: `ssfm-v21`, `ssfm-v30`. |
| `language` | string | no | ISO 639-3 language code for synthesis. |
| `prompt` | object | no | Emotion and style settings for the generated speech. |
| `output` | object | no | Audio output settings for the generated speech. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt.emotionType` | list | no | Prompt mode for emotion control. One of: `preset`, `smart`. |
| `prompt.emotionPreset` | list | no | Emotion preset to apply. One of: `angry`, `happy`, `normal`, `sad`, `tonedown`, `toneup`, `whisper`. |
| `prompt.emotionIntensity` | number | no | Strength of the emotional expression. |
| `prompt.previousText` | string | no | Text that comes before the generated text for smart emotion inference. |
| `prompt.nextText` | string | no | Text that comes after the generated text for smart emotion inference. |
| `output.audioPitch` | number | no | Pitch shift in semitones. |
| `output.audioTempo` | number | no | Speech speed multiplier. |
| `output.audioFormat` | list | no | Output audio format. One of: `mp3`, `wav`. Default: `wav`. |
| `seed` | number | no | Random seed for speech variation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TypeCast API returns.

## Native endpoint

Through the native TypeCast API, this operation is `POST /v1/text-to-speech/stream` (base URL `https://api.typecast.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/streaming-text-to-speech.md) for the provider-specific parameters and requirements.

