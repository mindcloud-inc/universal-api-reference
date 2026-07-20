# Uberduck: Text To Speech

Creates speech audio in Uberduck from input text.

```
POST https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uberduck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | The text to convert to speech. |
| `voice` | string | yes | The voice ID to use for speech generation. |
| `model` | string | no | Optional model ID. If omitted, Uberduck selects a compatible default model. |
| `outputFormat` | string | no | Optional output format such as mp3. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extended` | string | no | Optional JSON object for shared advanced controls such as speed, pitch, or emotion. |
| `modelSpecific` | string | no | Optional JSON object for model-specific controls such as Polly engine or Google speaking rate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string | URL of the generated audio file. |

## Native endpoint

Through the native Uberduck API, this operation is `POST /v1/text-to-speech` (base URL `https://api.uberduck.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-speech.md) for the provider-specific parameters and requirements.

