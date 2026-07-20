# Griptape: Get Bucket Asset URL

Retrieves a signed bucket asset URL from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket-asset-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket-asset-url?connectionId=$CONNECTION_ID&bucketId=string&fullKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "fullKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket-asset-url?${params}`, {
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
| `bucketId` | string | yes | The bucket ID containing the asset. |
| `fullKey` | string | yes | The full asset key to generate a URL for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "headers": {
        "x-ms-blob-type": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `headers.x-ms-blob-type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/buckets/:bucket_id/asset-urls/:full_key` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bucket-asset-url.md) for the provider-specific parameters and requirements.

