# ElevenLabs: Create Sound Effect

Creates sound effect audio from text in ElevenLabs.

```
POST https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-sound-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-sound-effect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-sound-effect', {
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
| `text` | string | yes | Text prompt describing the sound effect to generate. |
| `durationSeconds` | number | no | Approximate desired length of the generated sound effect in seconds. |
| `promptInfluence` | number | no | How strongly the prompt should influence the output. |
| `loop` | boolean | no | Whether the generated sound effect should loop seamlessly. |
| `modelId` | string | no | Optional sound generation model identifier. |
| `outputFormat` | string | no | Requested audio output format. Default: `mp3_44100_128`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `POST /sound-generation` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sound-effect.md) for the provider-specific parameters and requirements.

