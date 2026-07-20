# XenForo: Get Forum

Retrieves the specified forum from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum?connectionId=$CONNECTION_ID&id=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum?${params}`, {
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
| `id` | number | yes | ID of the forum to retrieve. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forum": {
        "description": "string",
        "node_id": 1,
        "title": "string",
        "view_url": "https://example.com"
      },
      "pagination": {
        "current_page": 1,
        "total": 1
      },
      "threads": [
        {
          "thread_id": 1,
          "title": "string",
          "username": "Ava Chen"
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
| `forum.description` | string |  |
| `forum.node_id` | number |  |
| `forum.title` | string |  |
| `forum.view_url` | string |  |
| `pagination.current_page` | number |  |
| `pagination.total` | number |  |
| `threads` | array<object> |  |
| `threads[].thread_id` | number |  |
| `threads[].title` | string |  |
| `threads[].username` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /forums/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forum.md) for the provider-specific parameters and requirements.

