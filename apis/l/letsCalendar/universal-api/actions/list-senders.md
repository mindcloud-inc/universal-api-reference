# Let's Calendar: List Senders

Retrieves sender emails from Let's Calendar.

```
GET https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders?${params}`, {
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
      "senderEmails": [
        {
          "email": "ava@example.com",
          "id": 1,
          "name": "ava@example.com",
          "providerName": "ava@example.com",
          "replyTo": "ava@example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `senderEmails[].email` | string |  |
| `senderEmails[].id` | number |  |
| `senderEmails[].name` | string |  |
| `senderEmails[].providerName` | string |  |
| `senderEmails[].replyTo` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `GET sender-emails` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-senders.md) for the provider-specific parameters and requirements.

