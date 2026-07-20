# Runway: Generate Sound Effects

Creates a sound effect generation task in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/generate-sound-effects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/generate-sound-effects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "eleven_text_to_sound_v2",
  "promptText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/generate-sound-effects', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "eleven_text_to_sound_v2",
    "promptText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | no | Optional sound duration in seconds, between 0.5 and 30. |
| `loop` | boolean | no | Whether the generated sound should loop seamlessly. |
| `model` | string | yes | Runway currently requires eleven_text_to_sound_v2. Default: `eleven_text_to_sound_v2`. |
| `promptText` | string | yes | Description of the sound effect to generate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "error": "string",
      "id": "string",
      "progress": 1,
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `error` | string |  |
| `id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/sound_effect` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-sound-effects.md) for the provider-specific parameters and requirements.

