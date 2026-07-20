# Appwrite: Delete bucket

Deletes the bucket from your Appwrite project.

```
DELETE https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-delete-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-delete-bucket?connectionId=$CONNECTION_ID&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-delete-bucket?${params}`, {
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
| `bucketId` | string | yes | Bucket unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the request succeeds. |

## Native endpoint

Through the native Appwrite API, this operation is `DELETE /storage/buckets/{bucketId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-delete-bucket.md) for the provider-specific parameters and requirements.

