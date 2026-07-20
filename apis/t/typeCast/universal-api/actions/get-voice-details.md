# TypeCast: Get Voice Details

Retrieves details for a specific voice from TypeCast.

```
GET https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-voice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TypeCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-voice-details?connectionId=$CONNECTION_ID&voiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-voice-details?${params}`, {
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
| `voiceId` | list | yes | Unique TypeCast voice identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": "string",
      "gender": "string",
      "models": [
        {
          "emotions": [
            "string"
          ],
          "version": "string"
        }
      ],
      "useCases": [
        "string"
      ],
      "voiceId": "string",
      "voiceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string | Voice age group classification when available. |
| `gender` | string | Voice gender classification when available. |
| `models` | array<object> | Supported TTS models for the voice. |
| `models[].emotions` | array<string> | Emotion presets supported by the model. |
| `models[].version` | string | Supported TTS model version. |
| `useCases` | array<string> | Voice use case categories. |
| `voiceId` | string | Unique TypeCast voice identifier. |
| `voiceName` | string | Human-readable voice name. |

## Native endpoint

Through the native TypeCast API, this operation is `GET /v2/voices/:voice_id` (base URL `https://api.typecast.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice-details.md) for the provider-specific parameters and requirements.

