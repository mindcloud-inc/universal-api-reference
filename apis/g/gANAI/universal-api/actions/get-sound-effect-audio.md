# GAN.AI: Get Sound Effect Audio

Retrieves Base64 audio for a sound effect in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-sound-effect-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-sound-effect-audio?connectionId=$CONNECTION_ID&inferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-sound-effect-audio?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inferenceId` | string | yes |  |

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

Through the native GAN.AI API, this operation is `POST /v1/sfx/audio` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sound-effect-audio.md) for the provider-specific parameters and requirements.

