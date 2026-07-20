# SeaTable: Mark Notification Read/Unread

Marks a SeaTable notification as read or unread.

```
PUT https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/mark-notification-read-unread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/mark-notification-read-unread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notificationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/mark-notification-read-unread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notificationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notificationId` | string | yes | The SeaTable notification ID. |

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

Through the native SeaTable API, this operation is `PUT /api-gateway/api/v2/dtables/:base_uuid/notifications/:notification_id/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notification-read-unread.md) for the provider-specific parameters and requirements.

