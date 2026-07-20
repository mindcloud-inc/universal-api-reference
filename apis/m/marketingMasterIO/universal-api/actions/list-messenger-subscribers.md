# Marketing Master IO: List Messenger Subscribers

Retrieves Messenger subscribers from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-messenger-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-messenger-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-messenger-subscribers?${params}`, {
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
| `page_id` | string | no | Filter subscribers by Facebook page ID. |

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
      "user_data": true
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
| `user_data` | boolean |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/messenger/subscriber` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messenger-subscribers.md) for the provider-specific parameters and requirements.

