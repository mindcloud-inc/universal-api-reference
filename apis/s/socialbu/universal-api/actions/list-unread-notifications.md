# Socialbu: List Unread Notifications

Retrieves unread notifications from SocialBu.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-unread-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-unread-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-unread-notifications?${params}`, {
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
      "created_at": "string",
      "currentPage": 1,
      "id": 1,
      "items": [
        {}
      ],
      "lastPage": 1,
      "message": "string",
      "nextPage": 1,
      "title": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `currentPage` | number |  |
| `id` | number |  |
| `items` | array<object> |  |
| `lastPage` | number |  |
| `message` | string |  |
| `nextPage` | number |  |
| `title` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /notifications/unread` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unread-notifications.md) for the provider-specific parameters and requirements.

