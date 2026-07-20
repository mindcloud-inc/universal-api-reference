# Yeti Snow: List Site History



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-site-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-site-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-site-history?${params}`, {
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
| `page` | string | no | Page number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {}
      ],
      "first_page_url": "https://example.com",
      "from": 1,
      "last_page": 1,
      "last_page_url": "https://example.com",
      "links": [
        {}
      ],
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1,
      "total_shr": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `data` | array<object> |  |
| `first_page_url` | string |  |
| `from` | number |  |
| `last_page` | number |  |
| `last_page_url` | string |  |
| `links` | array<object> |  |
| `next_page_url` | string |  |
| `path` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `to` | number |  |
| `total` | number |  |
| `total_shr` | number |  |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET history/site/index` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-history.md) for the provider-specific parameters and requirements.

