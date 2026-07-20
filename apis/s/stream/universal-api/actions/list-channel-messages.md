# Stream: List Channel Messages

Retrieves messages from a specific channel in Stream.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-channel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID&type=string&id=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "id": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/list-channel-messages?${params}`, {
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
| `type` | string | yes | Channel type. |
| `id` | string | yes | Channel ID. |
| `ids` | string<string> | yes | List of message IDs to fetch. |

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

Through the native Stream API, this operation is `GET /channels/:type/:id/messages` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-messages.md) for the provider-specific parameters and requirements.

