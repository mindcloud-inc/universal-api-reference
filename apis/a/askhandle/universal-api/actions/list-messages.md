# AskHandle: List Messages

Retrieves message records from your AskHandle account.

```
GET https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-messages?${params}`, {
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
      "body": "string",
      "email": "ava@example.com",
      "isSupportSender": true,
      "nickname": "Ava Chen",
      "phoneNumber": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "supportAnswer": "string",
      "terminated": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Message body. |
| `email` | string | Message sender email. |
| `isSupportSender` | boolean | Whether the sender is support. |
| `nickname` | string | Message sender nickname. |
| `phoneNumber` | string | Sender phone number. |
| `sentAt` | date | Sent timestamp. |
| `supportAnswer` | string | AskHandle support answer. |
| `terminated` | boolean | Whether the session is terminated. |
| `uuid` | string | Message UUID. |

## Native endpoint

Through the native AskHandle API, this operation is `GET /messages/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

