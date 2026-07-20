# Stream: List Message Replies

Retrieves replies from a message thread in Stream.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-message-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-message-replies?connectionId=$CONNECTION_ID&parentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-message-replies?${params}`, {
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
| `parentId` | string | yes | Parent message ID. |
| `limit` | number | no | Maximum number of replies to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "messages": [
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
| `duration` | string |  |
| `messages` | array<object> |  |

## Native endpoint

Through the native Stream API, this operation is `GET /messages/:parent_id/replies` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-replies.md) for the provider-specific parameters and requirements.

