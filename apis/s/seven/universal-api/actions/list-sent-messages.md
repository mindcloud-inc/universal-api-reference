# Seven: List Sent Messages

Retrieves sent messages from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-sent-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-sent-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-sent-messages?${params}`, {
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
      "channel": "string",
      "connection": "string",
      "dlr": "string",
      "dlr_timestamp": "2026-05-07T12:00:00.000Z",
      "foreign_id": "string",
      "from": "string",
      "id": "string",
      "label": "string",
      "latency": "string",
      "mccmnc": "string",
      "price": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `connection` | string |  |
| `dlr` | string |  |
| `dlr_timestamp` | date |  |
| `foreign_id` | string |  |
| `from` | string |  |
| `id` | string |  |
| `label` | string |  |
| `latency` | string |  |
| `mccmnc` | string |  |
| `price` | string |  |
| `text` | string |  |
| `timestamp` | date |  |
| `to` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /journal/outbound` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sent-messages.md) for the provider-specific parameters and requirements.

