# Seven: List Received SMS

Retrieves received SMS messages from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-received-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-received-sms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-received-sms?${params}`, {
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
      "from": "string",
      "id": "string",
      "price": "string",
      "reply_to_message_id": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string |  |
| `id` | string |  |
| `price` | string |  |
| `reply_to_message_id` | string |  |
| `text` | string |  |
| `timestamp` | date |  |
| `to` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /journal/inbound` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-received-sms.md) for the provider-specific parameters and requirements.

