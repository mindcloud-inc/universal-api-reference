# Habitica: Read Notifications

Marks notifications as read in Habitica.

```
PUT https://connect.mindcloud.co/v1/universal/habitica/latest/actions/read-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/read-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notificationIds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/habitica/latest/actions/read-notifications', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notificationIds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notificationIds` | list<string> | yes | The Habitica notification IDs to mark as read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "data": [
        {}
      ],
      "notifications": [
        {}
      ],
      "success": true,
      "userV": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `data` | array<object> |  |
| `notifications` | array<object> |  |
| `success` | boolean |  |
| `userV` | number |  |

## Native endpoint

Through the native Habitica API, this operation is `POST /notifications/read` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-notifications.md) for the provider-specific parameters and requirements.

