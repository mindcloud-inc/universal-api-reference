# deAPI: Calculate Text-to-Speech Price

Calculates text-to-speech request pricing in deAPI.

```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-speech-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-speech-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-speech-price?${params}`, {
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
| `format` | string | no | Audio output format such as mp3 or flac. |
| `lang` | string | no | Language code such as en-us. |
| `mode` | string | no | TTS mode. Use custom_voice for preset voices. |
| `model` | string | no | Speech model slug from List Models. |
| `sampleRate` | string | no | Sample rate for generated audio. |
| `speed` | string | no | Speech speed multiplier. |
| `text` | string | no | Text to estimate for speech generation. |
| `voice` | string | no | Voice slug for custom_voice mode. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2audio/price-calculation` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-text-to-speech-price.md) for the provider-specific parameters and requirements.

