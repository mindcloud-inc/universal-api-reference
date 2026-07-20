# Sendible: List Queues



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-queues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-queues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-queues?${params}`, {
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
      "id": 1,
      "is_paused": true,
      "queue_name": "Ava Chen",
      "queue_times": [
        {}
      ],
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_paused` | boolean |  |
| `queue_name` | string |  |
| `queue_times` | array<object> |  |
| `user_id` | number |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 1.0/api/queues` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queues.md) for the provider-specific parameters and requirements.

