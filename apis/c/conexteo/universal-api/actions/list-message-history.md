# Conexteo: List Message History

Finds message history in Conexteo.

```
GET https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-message-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-message-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-message-history?${params}`, {
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
      "content": "string",
      "credits_required": 1,
      "id": 1,
      "message_type": {},
      "recipients_count": 1,
      "scheduledate": "2026-05-07T12:00:00.000Z",
      "scheduletime": "string",
      "scheduletimestamp": "2026-05-07T12:00:00.000Z",
      "sender": "string",
      "shorturl_mode": {},
      "shorturl_url": "https://example.com",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Message content. |
| `credits_required` | number | Credits required for the message. |
| `id` | number | Message identifier. |
| `message_type` | object | Provider message-type payload. |
| `recipients_count` | number | Recipient count. |
| `scheduledate` | date | Scheduled send date. |
| `scheduletime` | string | Scheduled send time in HH:MM:SS format. |
| `scheduletimestamp` | date | Scheduled send timestamp. |
| `sender` | string | Configured sender value. |
| `shorturl_mode` | object | Short URL mode payload. |
| `shorturl_url` | string | Short URL target. |
| `state` | string | Provider message state. |

## Native endpoint

Through the native Conexteo API, this operation is `GET /messages` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-message-history.md) for the provider-specific parameters and requirements.

