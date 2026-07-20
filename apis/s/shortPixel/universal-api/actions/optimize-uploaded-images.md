# ShortPixel: Optimize Uploaded Images

Creates optimized image results from uploaded files in ShortPixel.

```
POST https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-uploaded-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShortPixel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-uploaded-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file1": "string",
  "filePaths": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-uploaded-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file1": "string",
    "filePaths": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file1` | file | yes | The local image file to upload for optimization. |
| `filePaths` | object | yes | JSON object whose keys match uploaded file field names and whose values are source paths meaningful to you, for example {"file1":"/images/source.jpg"}. |
| `lossy` | number | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | number | no | Maximum seconds to wait for optimization before returning. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AVIFLosslessURL": "https://example.com",
      "AVIFLossyURL": "https://example.com",
      "Key": "string",
      "localPath": "string",
      "LoselessSize": 1,
      "LosslessURL": "https://example.com",
      "LossySize": 1,
      "LossyURL": "https://example.com",
      "OriginalSize": 1,
      "OriginalURL": "https://example.com",
      "Status": {},
      "Timestamp": "string",
      "Unlimited": true,
      "WebPLosslessURL": "https://example.com",
      "WebPLossyURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AVIFLosslessURL` | string | Download URL for the lossless AVIF result when requested. |
| `AVIFLossyURL` | string | Download URL for the lossy or glossy AVIF result when requested. |
| `Key` | string | Uploaded multipart field name echoed by ShortPixel. |
| `localPath` | string | Provider-side local processing path echoed by ShortPixel. |
| `LoselessSize` | number | Lossless optimized file size in bytes. |
| `LosslessURL` | string | Download URL for the lossless optimized image when available. |
| `LossySize` | number | Lossy or glossy optimized file size in bytes. |
| `LossyURL` | string | Download URL for the lossy or glossy optimized image when available. |
| `OriginalSize` | number | Original file size in bytes. |
| `OriginalURL` | string | Temporary URL for the uploaded source image or upload reference. |
| `Status` | object | Optimization status object with provider code and message. |
| `Timestamp` | string | Provider processing timestamp. |
| `Unlimited` | boolean | Whether the processed item used an unlimited account allowance. |
| `WebPLosslessURL` | string | Download URL for the lossless WebP result when requested. |
| `WebPLossyURL` | string | Download URL for the lossy or glossy WebP result when requested. |

## Native endpoint

Through the native ShortPixel API, this operation is `POST /v2/post-reducer.php` (base URL `https://api.shortpixel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/optimize-uploaded-images.md) for the provider-specific parameters and requirements.

