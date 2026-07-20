# Marketing Master IO: Get Messenger Subscriber

Retrieves a Messenger subscriber from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-messenger-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-messenger-subscriber?connectionId=$CONNECTION_ID&subscriber_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriber_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-messenger-subscriber?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriber_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "gender": "string",
      "is_bot_subscriber": "string",
      "last_interaction_time": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "locale": "string",
      "page_id": "string",
      "subscribed_at": "2026-05-07T12:00:00.000Z",
      "subscriber_id": "string",
      "tags": "string",
      "timezone": "string",
      "user_data": {
        "order": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `gender` | string |  |
| `is_bot_subscriber` | string |  |
| `last_interaction_time` | date |  |
| `last_name` | string |  |
| `locale` | string |  |
| `page_id` | string |  |
| `subscribed_at` | date |  |
| `subscriber_id` | string |  |
| `tags` | string |  |
| `timezone` | string |  |
| `user_data.order` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/messenger/subscriber/:subscriber_id` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messenger-subscriber.md) for the provider-specific parameters and requirements.

