# ElevenLabs: Create Dialogue

Creates dialogue audio from text in ElevenLabs.

```
POST https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-dialogue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-dialogue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs[]": [
    {}
  ],
  "inputs[].text": "string",
  "inputs[].voiceId": "string",
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-dialogue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs[]": [{}],
    "inputs[].text": "string",
    "inputs[].voiceId": "string",
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputs[]` | array<object> | yes | Dialogue turns in order. |
| `inputs[].text` | string | yes |  |
| `inputs[].voiceId` | string | yes |  |
| `modelId` | string | yes |  |
| `outputFormat` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no |  |
| `seed` | number | no |  |
| `settings` | object | no |  |
| `settings.speed` | number | no |  |
| `applyTextNormalization` | string | no | Use auto, on, or off. |
| `pronunciationDictionaryLocators[]` | array<object> | no | Pronunciation dictionaries to apply. |
| `pronunciationDictionaryLocators[].id` | string | no |  |
| `pronunciationDictionaryLocators[].versionId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `POST /text-to-dialogue` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dialogue.md) for the provider-specific parameters and requirements.

