# Inoreader: List Unread Counters

Retrieves unread counters from Inoreader.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-unread-counters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-unread-counters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-unread-counters?${params}`, {
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
      "max": 1,
      "unreadcounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `max` | number | The maximum unread count limit returned by Inoreader. |
| `unreadcounts` | array<object> | Unread count entries keyed by stream or state identifier. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /unread-count` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unread-counters.md) for the provider-specific parameters and requirements.

