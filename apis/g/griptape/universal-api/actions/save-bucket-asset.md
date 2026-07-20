# Griptape: Save Bucket Asset

Creates a bucket asset record in Griptape.

```
PUT https://connect.mindcloud.co/v1/universal/griptape/latest/actions/save-bucket-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/save-bucket-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/save-bucket-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | The bucket ID to save the asset in. |
| `name` | string | yes | The full asset key to create in the bucket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "size": 1,
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
| `created_by` | string |  |
| `name` | string |  |
| `organization_id` | string |  |
| `size` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Griptape API, this operation is `PUT /api/buckets/:bucket_id/assets` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-bucket-asset.md) for the provider-specific parameters and requirements.

