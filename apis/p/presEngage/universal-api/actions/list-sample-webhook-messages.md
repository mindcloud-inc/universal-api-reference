# PresEngage: List Sample Webhook Messages

Retrieves sample webhook message data from PresEngage for setup.

```
GET https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/list-sample-webhook-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PresEngage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/list-sample-webhook-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/list-sample-webhook-messages?${params}`, {
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
      "message": {
        "content": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "deck_id": "string",
        "id": "string",
        "is_incoming": true,
        "participant_name": "Ava Chen",
        "phone_number": "string",
        "presentation_title": "string",
        "uuid": "string"
      },
      "subscription_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object |  |
| `message.content` | string |  |
| `message.created_at` | date |  |
| `message.deck_id` | string |  |
| `message.id` | string |  |
| `message.is_incoming` | boolean |  |
| `message.participant_name` | string |  |
| `message.phone_number` | string |  |
| `message.presentation_title` | string |  |
| `message.uuid` | string |  |
| `subscription_id` | string |  |

## Native endpoint

Through the native PresEngage API, this operation is `GET /hooks/performList` (base URL `https://shared.presengage.com/functions/v1/presengage-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sample-webhook-messages.md) for the provider-specific parameters and requirements.

