# Conexteo: List All Message Replies

Finds all message replies in Conexteo.

```
GET https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-all-message-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-all-message-replies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-all-message-replies?${params}`, {
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
| `content` | string | Reply content. |
| `credits_required` | number | Credits required for the related message. |
| `id` | number | Reply identifier. |
| `message_type` | object | Provider message-type payload. |
| `recipients_count` | number | Recipient count. |
| `scheduledate` | date | Scheduled send date. |
| `scheduletime` | string | Scheduled send time in HH:MM:SS format. |
| `scheduletimestamp` | date | Scheduled send timestamp. |
| `sender` | string | Sender value associated with the reply. |
| `shorturl_mode` | object | Short URL mode payload. |
| `shorturl_url` | string | Short URL target. |
| `state` | string | Provider reply state. |

## Native endpoint

Through the native Conexteo API, this operation is `GET /messages/replies/extract` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-message-replies.md) for the provider-specific parameters and requirements.

