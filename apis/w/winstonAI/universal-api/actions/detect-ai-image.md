# Winston AI: Detect AI Image



```
GET https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Winston AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-image?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fimage.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/image.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/detect-ai-image?${params}`, {
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
| `url` | string | yes | Public image URL to scan for AI generation signals. Example: `https://example.com/image.jpg`. |
| `version` | string | no | The Winston AI image model version to use. Example: `latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_probability": 1,
      "ai_watermark_detected": true,
      "ai_watermark_issuers": [
        "string"
      ],
      "c2pa": {},
      "credits_remaining": 1,
      "credits_used": 1,
      "exif": {},
      "human_probability": 1,
      "metadata": {},
      "mime_type": "string",
      "score": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_probability` | number | Probability that the image was created by AI. |
| `ai_watermark_detected` | boolean | Whether an AI watermark was detected. |
| `ai_watermark_issuers` | array<string> | Detected AI watermark issuers. |
| `c2pa` | object | C2PA provenance metadata when present. |
| `credits_remaining` | number | Remaining Winston AI credits after the scan. |
| `credits_used` | number | Credits consumed by the image scan. |
| `exif` | object | Extracted EXIF and related image metadata. |
| `human_probability` | number | Probability that the image was created by a human. |
| `metadata` | object | Technical image metadata such as dimensions and format. |
| `mime_type` | string | Mime type of the analyzed image. |
| `score` | number | Human-likelihood score for the scanned image. |
| `version` | string | Image model version used for the prediction. |

## Native endpoint

Through the native Winston AI API, this operation is `POST /v2/image-detection` (base URL `https://api.gowinston.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-ai-image.md) for the provider-specific parameters and requirements.

