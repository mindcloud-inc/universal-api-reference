# Shuffler: Clear Notifications

Marks all notifications as read in Shuffler.

```
PUT https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/clear-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/clear-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/clear-notifications', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `GET /notifications/clear` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-notifications.md) for the provider-specific parameters and requirements.

