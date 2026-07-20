# Stable Diffusion: Transform Audio From Audio

Transforms audio from an input clip in Stable Diffusion.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/transform-audio-from-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/transform-audio-from-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/transform-audio-from-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio` | string | yes | Source audio clip to transform. |
| `prompt` | string | yes | Text prompt describing the transformed audio output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": "string",
      "finish_reason": "string",
      "seed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | string |  |
| `finish_reason` | string |  |
| `seed` | number |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `POST /v2beta/audio/stable-audio-2/audio-to-audio` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transform-audio-from-audio.md) for the provider-specific parameters and requirements.

