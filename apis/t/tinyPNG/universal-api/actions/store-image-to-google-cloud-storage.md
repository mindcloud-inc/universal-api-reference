# TinyPNG: Store Image To Google Cloud Storage

Stores a TinyPNG image in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-google-cloud-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TinyPNG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-google-cloud-storage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputPath": "/output/abc123",
  "gcpAccessToken": "ya29.c.ExampleToken",
  "path": "example-bucket/my-images/optimized.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-google-cloud-storage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputPath": "/output/abc123",
    "gcpAccessToken": "ya29.c.ExampleToken",
    "path": "example-bucket/my-images/optimized.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputPath` | string | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. Example: `/output/abc123`. |
| `gcpAccessToken` | string | yes | Short-lived Google Cloud access token generated from a service account. Example: `ya29.c.ExampleToken`. |
| `path` | string | yes | Destination path in the format <bucket>/<path>/<filename>. Example: `example-bucket/my-images/optimized.jpg`. |
| `cacheControl` | string | no | Optional Cache-Control header value to apply on the stored object. Example: `public, max-age=31536000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compressionCount": 1,
      "imageHeight": 1,
      "imageWidth": 1,
      "location": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compressionCount` | number |  |
| `imageHeight` | number |  |
| `imageWidth` | number |  |
| `location` | string |  |

## Native endpoint

Through the native TinyPNG API, this operation is `POST {{outputPath}}` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-image-to-google-cloud-storage.md) for the provider-specific parameters and requirements.

