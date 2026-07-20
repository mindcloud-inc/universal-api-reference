# ntfy: Subscribe Multiple Topics SSE Stream

Subscribes to multiple ntfy topics as an SSE stream.

```
GET https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-multiple-topics-sse-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ntfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-multiple-topics-sse-stream?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-multiple-topics-sse-stream?${params}`, {
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
      "data": "string",
      "event": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | SSE data payload emitted by ntfy. |
| `event` | string | SSE event name emitted by ntfy. |

## Native endpoint

Through the native ntfy API, this operation is `GET /:topics/sse` (base URL `https://ntfy.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-multiple-topics-sse-stream.md) for the provider-specific parameters and requirements.

