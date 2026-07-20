# Uniqode: List Tags

Retrieves tags from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-tags?${params}`, {
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
          "child_tags": [
            {}
          ],
          "color": "string",
          "created": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "maintainer": 1,
          "name": "Ava Chen",
          "organization": 1,
          "product_type": "string",
          "qrcode_count": 1,
          "qrcode_data": [
            {}
          ],
          "qrcode_set": [
            {}
          ],
          "slug": "string",
          "updated": "2026-05-07T12:00:00.000Z"
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
| `results[].child_tags` | array<object> |  |
| `results[].color` | string |  |
| `results[].created` | date |  |
| `results[].id` | number |  |
| `results[].maintainer` | number |  |
| `results[].name` | string |  |
| `results[].organization` | number |  |
| `results[].product_type` | string |  |
| `results[].qrcode_count` | number |  |
| `results[].qrcode_data` | array<object> |  |
| `results[].qrcode_set` | array<object> |  |
| `results[].slug` | string |  |
| `results[].updated` | date |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /tags/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

