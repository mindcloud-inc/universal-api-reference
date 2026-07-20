# Svix: Poller Sink Stream Events

Retrieves stream events from a Svix sink.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/poller-sink-stream-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/poller-sink-stream-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/poller-sink-stream-events?${params}`, {
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
      "data": [
        {}
      ],
      "done": true,
      "iterator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `done` | boolean |  |
| `iterator` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/stream/{stream_id}/sink/{sink_id}/events` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poller-sink-stream-events.md) for the provider-specific parameters and requirements.

