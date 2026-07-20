# ShortPixel: Optimize Remote Images

Creates optimized image results from remote URLs in ShortPixel.

```
POST https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShortPixel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrls[]` | array<string> | yes | One or more publicly reachable image URLs to optimize. |
| `lossy` | number | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | number | no | Maximum seconds to wait for optimization before returning. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AVIFLosslessSize": "string",
      "AVIFLosslessURL": "https://example.com",
      "AVIFLossySize": "string",
      "AVIFLossyURL": "https://example.com",
      "LoselessSize": 1,
      "LosslessSize": 1,
      "LosslessURL": "https://example.com",
      "LossySize": 1,
      "LossyURL": "https://example.com",
      "OriginalSize": 1,
      "OriginalURL": "https://example.com",
      "PercentImprovement": "string",
      "Status": {},
      "TimeStamp": "string",
      "Unlimited": true,
      "WebPLoselessSize": "string",
      "WebPLosslessSize": "string",
      "WebPLosslessURL": "https://example.com",
      "WebPLossySize": "string",
      "WebPLossyURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AVIFLosslessSize` | string | Lossless AVIF size or NA. |
| `AVIFLosslessURL` | string | Download URL for the lossless AVIF result when requested. |
| `AVIFLossySize` | string | Lossy AVIF size or NA. |
| `AVIFLossyURL` | string | Download URL for the lossy or glossy AVIF result when requested. |
| `LoselessSize` | number | Legacy misspelled provider alias for lossless optimized size. |
| `LosslessSize` | number | Lossless optimized file size in bytes. |
| `LosslessURL` | string | Download URL for the lossless optimized image when available. |
| `LossySize` | number | Lossy or glossy optimized file size in bytes. |
| `LossyURL` | string | Download URL for the lossy or glossy optimized image when available. |
| `OriginalSize` | number | Original file size in bytes. |
| `OriginalURL` | string | The original source image URL. |
| `PercentImprovement` | string | Reported percentage size improvement. |
| `Status` | object | Optimization status object with provider code and message. |
| `TimeStamp` | string | Provider processing timestamp. |
| `Unlimited` | boolean | Whether the processed item used an unlimited account allowance. |
| `WebPLoselessSize` | string | Legacy misspelled provider alias for lossless WebP size or NA. |
| `WebPLosslessSize` | string | Lossless WebP size or NA. |
| `WebPLosslessURL` | string | Download URL for the lossless WebP result when requested. |
| `WebPLossySize` | string | Lossy WebP size or NA. |
| `WebPLossyURL` | string | Download URL for the lossy or glossy WebP result when requested. |

## Native endpoint

Through the native ShortPixel API, this operation is `POST /v2/reducer.php` (base URL `https://api.shortpixel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/optimize-remote-images.md) for the provider-specific parameters and requirements.

