# Uniqode: List Media Objects

Retrieves media objects from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-media-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-media-objects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-media-objects?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {
          "content_type": "string",
          "created": "2026-05-07T12:00:00.000Z",
          "folder": 1,
          "id": 1,
          "maintainer": 1,
          "modified": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "organization": 1,
          "s3_object_key": "string",
          "status": "string",
          "typeform_compatible": true,
          "typeform_url": "https://example.com",
          "url": "https://example.com",
          "visible": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `results[].content_type` | string |  |
| `results[].created` | date |  |
| `results[].folder` | number |  |
| `results[].id` | number |  |
| `results[].maintainer` | number |  |
| `results[].modified` | date |  |
| `results[].name` | string |  |
| `results[].organization` | number |  |
| `results[].s3_object_key` | string |  |
| `results[].status` | string |  |
| `results[].typeform_compatible` | boolean |  |
| `results[].typeform_url` | string |  |
| `results[].url` | string |  |
| `results[].visible` | boolean |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /media/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media-objects.md) for the provider-specific parameters and requirements.

