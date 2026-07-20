# Stability AI: Inpaint Audio

Updates audio in Stability AI with inpainting.

```
PUT https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/inpaint-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/inpaint-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/inpaint-audio', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "audio": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Text prompt describing the desired audio inpaint. |
| `audio` | file | yes | Source audio file to inpaint. |

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
| `audio` | string | Generated audio encoded as base64. |
| `finish_reason` | string | Reason the generation finished. |
| `seed` | number | Seed used for the generation. |

## Native endpoint

Through the native Stability AI API, this operation is `POST /v2beta/audio/stable-audio-2/inpaint` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inpaint-audio.md) for the provider-specific parameters and requirements.

