# Runway: Text To Speech

Creates a text-to-speech generation task in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "eleven_multilingual_v2",
  "promptText": "string",
  "voice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "eleven_multilingual_v2",
    "promptText": "string",
    "voice": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Runway currently requires eleven_multilingual_v2. Default: `eleven_multilingual_v2`. |
| `promptText` | string | yes | Detailed prompt text to synthesize into speech. |
| `voice` | object | yes | Voice object with type runway-preset and presetId. |

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

Through the native Runway API, this operation is `POST /v1/text_to_speech` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-speech.md) for the provider-specific parameters and requirements.

