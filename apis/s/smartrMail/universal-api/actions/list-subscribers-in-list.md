# SmartrMail: List Subscribers in List

Retrieves subscribers from a specific SmartrMail list.

```
GET https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscribers-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartrMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscribers-in-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscribers-in-list?${params}`, {
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
| `listId` | string | yes | The ID of the requested list. |

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

Through the native SmartrMail API, this operation is `GET /lists/:list_id/list_subscribers` (base URL `https://go.smartrmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers-in-list.md) for the provider-specific parameters and requirements.

