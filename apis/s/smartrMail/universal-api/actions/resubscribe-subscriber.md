# SmartrMail: Resubscribe Subscriber

Resubscribes a subscriber in SmartrMail by identifier.

```
PUT https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/resubscribe-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartrMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/resubscribe-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/resubscribe-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriberIdentifier` | string | yes | The subscriber email address, phone number, or UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicked_count": 1,
      "complained": true,
      "custom_fields": [
        {}
      ],
      "delivered_count": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "joined_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "opened_count": 1,
      "phone": "string",
      "subscribed": true,
      "unsubscribed_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicked_count` | number |  |
| `complained` | boolean |  |
| `custom_fields` | array<object> |  |
| `delivered_count` | number |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `joined_at` | date |  |
| `last_name` | string |  |
| `opened_count` | number |  |
| `phone` | string |  |
| `subscribed` | boolean |  |
| `unsubscribed_at` | date |  |

## Native endpoint

Through the native SmartrMail API, this operation is `POST /subscribers/:email_or_phone_or_uid/resubscribe` (base URL `https://go.smartrmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resubscribe-subscriber.md) for the provider-specific parameters and requirements.

