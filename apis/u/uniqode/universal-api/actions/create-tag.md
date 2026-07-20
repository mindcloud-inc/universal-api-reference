# Uniqode: Create Tag

Creates a new tag in Uniqode.

```
POST https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child_tags` | array<object> |  |
| `color` | string |  |
| `created` | date |  |
| `id` | number |  |
| `maintainer` | number |  |
| `name` | string |  |
| `organization` | number |  |
| `product_type` | string |  |
| `qrcode_count` | number |  |
| `qrcode_data` | array<object> |  |
| `qrcode_set` | array<object> |  |
| `slug` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Uniqode API, this operation is `POST /tags/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

