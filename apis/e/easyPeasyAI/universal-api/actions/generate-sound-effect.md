# Easy-Peasy.AI: Generate Sound Effect

Generates a sound effect in Easy-Peasy.AI.

```
POST https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-sound-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-sound-effect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-sound-effect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | The text prompt describing the sound effect to generate. |
| `duration` | number | no | Optional target duration for the sound effect. |
| `promptInfluence` | number | no | Optional prompt adherence level from 0.0 to 1.0. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `POST /api/generate-sound` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-sound-effect.md) for the provider-specific parameters and requirements.

