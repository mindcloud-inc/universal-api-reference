# Sendcrux: List Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-subscriptions?${params}`, {
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
| `page` | string | no | The page number of subscriptions to return. |
| `per_page` | string | no | The number of subscriptions to return per page. |

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
      "total": 1
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

## Native endpoint

Through the native Sendcrux API, this operation is `GET /api/v1/subscriptions` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

