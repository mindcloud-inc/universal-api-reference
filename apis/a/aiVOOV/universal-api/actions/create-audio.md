# AiVOOV: Create Audio

Creates audio from multiple voice and text inputs in AiVOOV.

```
POST https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/create-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiVOOV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/create-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceIds": "string",
  "texts[]": "Hello from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/create-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceIds": "string",
    "texts[]": "Hello from MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceIds` | list<string> | yes | Select one or more voice IDs to synthesize. Accepts multiple values as an array. |
| `texts[]` | array<string> | yes | Enter the text for each selected voice in matching order. Example: `Hello from MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pitchRates[]` | array<string> | no | Optional pitch adjustment for each text item, or default. Example: `default`. |
| `speakingRates[]` | array<string> | no | Optional speaking-rate adjustment for each text item, or default. Example: `default`. |
| `volumes[]` | array<string> | no | Optional volume adjustment for each text item, or default. Example: `default`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AiVOOV API returns.

## Native endpoint

Through the native AiVOOV API, this operation is `POST /create` (base URL `https://aivoov.com/api/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audio.md) for the provider-specific parameters and requirements.

