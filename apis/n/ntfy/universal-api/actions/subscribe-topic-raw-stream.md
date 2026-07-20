# ntfy: Subscribe Topic Raw Stream

Subscribes to an ntfy topic as a raw stream.

```
GET https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-topic-raw-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ntfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-topic-raw-stream?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/subscribe-topic-raw-stream?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Raw message text line returned by the topic raw stream. |

## Native endpoint

Through the native ntfy API, this operation is `GET /:topic/raw` (base URL `https://ntfy.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-topic-raw-stream.md) for the provider-specific parameters and requirements.

