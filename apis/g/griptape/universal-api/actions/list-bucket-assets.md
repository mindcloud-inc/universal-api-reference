# Griptape: List Bucket Assets

Finds assets in a Griptape bucket.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-bucket-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-bucket-assets?connectionId=$CONNECTION_ID&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-bucket-assets?${params}`, {
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
| `bucketId` | string | yes | The bucket ID whose assets should be listed. |
| `postfix` | string | no | Optional asset key postfix to filter results. |
| `prefix` | string | no | Optional asset key prefix to filter results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": [
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
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      },
      "prefix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets[].bucket_id` | string |  |
| `assets[].created_at` | date |  |
| `assets[].created_by` | string |  |
| `assets[].name` | string |  |
| `assets[].organization_id` | string |  |
| `assets[].size` | number |  |
| `assets[].updated_at` | date |  |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |
| `prefix` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/buckets/:bucket_id/assets` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bucket-assets.md) for the provider-specific parameters and requirements.

