# WatermarkRemover.io: Generate AI Background

Generates an AI background for a file in WatermarkRemover.io.

```
GET https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/generate-ai-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WatermarkRemover.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/generate-ai-background?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/generate-ai-background?${params}`, {
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
| `cloudName` | string | no | PixelBin cloud name from the CDN URL. |
| `filePath` | string | no | Path to the image inside PixelBin storage. |
| `zone` | string | no | PixelBin zone slug from the CDN URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary response bytes for the generated image or document. |
| `type` | string | Runtime body type returned by PixelBin for binary transform responses. |

## Native endpoint

Through the native WatermarkRemover.io API, this operation is `GET /v2/[:cloudName]/[:zone]/generate.bg()/[:filePath]` (base URL `https://cdn.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ai-background.md) for the provider-specific parameters and requirements.

