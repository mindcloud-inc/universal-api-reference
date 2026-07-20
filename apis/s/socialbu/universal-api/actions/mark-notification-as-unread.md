# Socialbu: Mark Notification as Unread

Marks a notification as unread in SocialBu.

```
PUT https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/mark-notification-as-unread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/mark-notification-as-unread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/mark-notification-as-unread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "read": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `read` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Socialbu API, this operation is `POST /notifications/{id}/mark_unread` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notification-as-unread.md) for the provider-specific parameters and requirements.

