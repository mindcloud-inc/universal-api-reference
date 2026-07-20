# TinyPNG: Store Image To Amazon S3

Stores a TinyPNG image in Amazon S3.

```
POST https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-amazon-s3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TinyPNG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-amazon-s3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputPath": "/output/abc123",
  "awsAccessKeyId": "AKIAIOSFODNN7EXAMPLE",
  "awsSecretAccessKey": "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY",
  "region": "us-west-1",
  "path": "example-bucket/my-images/optimized.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/store-image-to-amazon-s3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputPath": "/output/abc123",
    "awsAccessKeyId": "AKIAIOSFODNN7EXAMPLE",
    "awsSecretAccessKey": "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY",
    "region": "us-west-1",
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
| `awsAccessKeyId` | string | yes | AWS access key ID used to upload the object. Example: `AKIAIOSFODNN7EXAMPLE`. |
| `awsSecretAccessKey` | string | yes | AWS secret access key used to upload the object. Example: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`. |
| `region` | string | yes | AWS region where the destination bucket is located. Example: `us-west-1`. |
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

Through the native TinyPNG API, this operation is `POST {{outputPath}}` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-image-to-amazon-s3.md) for the provider-specific parameters and requirements.

