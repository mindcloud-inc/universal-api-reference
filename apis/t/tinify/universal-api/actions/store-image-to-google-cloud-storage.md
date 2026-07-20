# Tinify: Store Image To Google Cloud Storage

Stores an optimized image from Tinify in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-google-cloud-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-google-cloud-storage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
  "store.gcp_access_token": "Google Cloud access token",
  "store.path": "example-bucket/my-images/optimized.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/store-image-to-google-cloud-storage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
    "store.gcp_access_token": "Google Cloud access token",
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
| `store.gcp_access_token` | string | yes | Google Cloud access token with permission to write to the target bucket path. Example: `Google Cloud access token`. |
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

Through the native Tinify API, this operation is `POST /output/:outputId` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-image-to-google-cloud-storage.md) for the provider-specific parameters and requirements.

