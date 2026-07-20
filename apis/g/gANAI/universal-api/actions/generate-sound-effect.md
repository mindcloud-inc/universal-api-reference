# GAN.AI: Generate Sound Effect

Creates generated sound effects in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/generate-sound-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/generate-sound-effect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/generate-sound-effect', {
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
| `creativity` | number | no |  |
| `durationSeconds` | number | no |  |
| `numVariations` | number | no |  |
| `prompt` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sfxInferenceHistoryObject": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "generationParams": {
          "creativity": 1,
          "durationSeconds": 1,
          "seed": "string"
        },
        "inferenceId": "string",
        "sfxPrompt": "string"
      },
      "wavBase64": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sfxInferenceHistoryObject.createdAt` | date |  |
| `sfxInferenceHistoryObject.generationParams.creativity` | number |  |
| `sfxInferenceHistoryObject.generationParams.durationSeconds` | number |  |
| `sfxInferenceHistoryObject.generationParams.seed` | string |  |
| `sfxInferenceHistoryObject.inferenceId` | string |  |
| `sfxInferenceHistoryObject.sfxPrompt` | string |  |
| `wavBase64` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/sfx/generate` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-sound-effect.md) for the provider-specific parameters and requirements.

