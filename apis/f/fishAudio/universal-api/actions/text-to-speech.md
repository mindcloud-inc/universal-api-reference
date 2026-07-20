# Fish Audio: Text to Speech

Converts text to speech with Fish Audio.

```
POST https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text to synthesize. |
| `referenceId` | string | no | Optional model ID or speaker reference ID. |
| `format` | list | no | Output audio format. One of: `0`, `1`, `2`. Default: `mp3`. |
| `sampleRate` | number | no | Output sample rate. Default: `44100`. |
| `mp3Bitrate` | number | no | MP3 bitrate when format is mp3. Default: `128`. |
| `normalize` | boolean | no | Normalize the generated audio. Default: `true`. |
| `temperature` | number | no | Sampling temperature. Default: `0.7`. |
| `topP` | number | no | Top-p sampling value. Default: `0.7`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fish Audio API returns.

## Native endpoint

Through the native Fish Audio API, this operation is `POST /v1/tts` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-speech.md) for the provider-specific parameters and requirements.

