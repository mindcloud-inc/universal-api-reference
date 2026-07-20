# Griptape: Get Bucket

Retrieves a bucket from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket?connectionId=$CONNECTION_ID&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-bucket?${params}`, {
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
| `bucketId` | string | yes | The bucket ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organization_default": true,
      "organization_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket_id` | string |  |
| `created_at` | date |  |
| `name` | string |  |
| `organization_default` | boolean |  |
| `organization_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/buckets/:bucket_id` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bucket.md) for the provider-specific parameters and requirements.

