# deAPI: Calculate Video Transcription Price



```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-transcription-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-transcription-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-transcription-price?${params}`, {
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
| `includeTs` | string | no | Whether the transcription should include timestamps. |
| `model` | string | no | Transcription model slug from List Models. |
| `sourceUrl` | string | no | Audio or video URL to price for transcription. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/transcribe/price-calculation` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-transcription-price.md) for the provider-specific parameters and requirements.

