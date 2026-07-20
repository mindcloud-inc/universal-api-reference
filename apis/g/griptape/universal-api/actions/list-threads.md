# Griptape: List Threads

Finds threads in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads?${params}`, {
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
| `alias` | string | no | Optional alias to filter the thread list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      },
      "threads": [
        {
          "alias": "string",
          "created_at": "string",
          "created_by": "string",
          "message_count": 1,
          "messages_length": 1,
          "metadata": {},
          "name": "Ava Chen",
          "organization_id": "string",
          "thread_id": "string",
          "updated_at": "string"
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
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |
| `threads[].alias` | string |  |
| `threads[].created_at` | string |  |
| `threads[].created_by` | string |  |
| `threads[].message_count` | number |  |
| `threads[].messages_length` | number |  |
| `threads[].metadata` | object |  |
| `threads[].name` | string |  |
| `threads[].organization_id` | string |  |
| `threads[].thread_id` | string |  |
| `threads[].updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/threads` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-threads.md) for the provider-specific parameters and requirements.

