# Tinify: Store Image To Amazon S3

Stores an optimized image from Tinify in Amazon S3.

```
POST https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-amazon-s3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-amazon-s3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
  "store.aws_access_key_id": "AKIA...",
  "store.aws_secret_access_key": "AWS secret access key",
  "store.region": "us-west-1",
  "store.path": "example-bucket/my-images/optimized.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-amazon-s3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
    "store.aws_access_key_id": "AKIA...",
    "store.aws_secret_access_key": "AWS secret access key",
    "store.region": "us-west-1",
    "store.path": "example-bucket/my-images/optimized.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputId` | string | yes | Tinify output identifier from a prior compression URL. Example: `zr1jp6xybr82ge0s683x67rgwsawjw4z`. |
| `store.aws_access_key_id` | string | yes | AWS access key ID with permission to put objects at the target path. Example: `AKIA...`. |
| `store.aws_secret_access_key` | string | yes | AWS secret access key for the S3 user. Example: `AWS secret access key`. |
| `store.region` | string | yes | AWS region for the S3 bucket, such as us-west-1. Example: `us-west-1`. |
| `store.path` | string | yes | Destination path in the format bucket/path/filename. Example: `example-bucket/my-images/optimized.jpg`. |

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
| `data` | array<number> | Response bytes returned by Tinify for the store operation. |
| `type` | string | Raw response object type for the store operation response. |

## Native endpoint

Through the native Tinify API, this operation is `POST /output/:outputId` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-image-to-amazon-s3.md) for the provider-specific parameters and requirements.

