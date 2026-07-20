# ExpertTexting: List Unread Inbox Messages

Retrieves unread inbox messages from ExpertTexting.

```
GET https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/list-unread-inbox-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ExpertTexting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/list-unread-inbox-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/list-unread-inbox-messages?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "sender": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Timestamp reported by ExpertTexting for the unread reply. |
| `sender` | string | Sender number for the unread reply. |
| `text` | string | Unread reply text. |

## Native endpoint

Through the native ExpertTexting API, this operation is `GET /ExptRestApi/sms/json/Message/UnreadInbox` (base URL `https://www.experttexting.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unread-inbox-messages.md) for the provider-specific parameters and requirements.

