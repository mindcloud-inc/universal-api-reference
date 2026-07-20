# Griptape: List Buckets

Finds buckets in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-buckets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "buckets": [
        {
          "bucket_id": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "organization_default": true,
          "organization_id": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buckets[].bucket_id` | string |  |
| `buckets[].created_at` | date |  |
| `buckets[].name` | string |  |
| `buckets[].organization_default` | boolean |  |
| `buckets[].organization_id` | string |  |
| `buckets[].updated_at` | date |  |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/buckets` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

