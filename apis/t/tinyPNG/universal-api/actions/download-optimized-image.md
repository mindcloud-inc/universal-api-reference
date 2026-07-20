# TinyPNG: Download Optimized Image

Downloads an optimized image from TinyPNG.

```
GET https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TinyPNG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputPath=%2Foutput%2Fabc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputPath": "/output/abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image?${params}`, {
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
| `outputPath` | string | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. Example: `/output/abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compressionCount": 1,
      "contentLength": 1,
      "contentType": "string",
      "imageHeight": 1,
      "imageWidth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compressionCount` | number |  |
| `contentLength` | number |  |
| `contentType` | string |  |
| `imageHeight` | number |  |
| `imageWidth` | number |  |

## Native endpoint

Through the native TinyPNG API, this operation is `GET {{outputPath}}` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-optimized-image.md) for the provider-specific parameters and requirements.

