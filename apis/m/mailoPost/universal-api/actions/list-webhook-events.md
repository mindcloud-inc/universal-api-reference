# MailoPost: List Webhook Events

Retrieves message webhook events from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-webhook-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-webhook-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-webhook-events?${params}`, {
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
      "events": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `GET /email/messages_webhooks/events` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-events.md) for the provider-specific parameters and requirements.

