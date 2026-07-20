# Instructure: Update Notification Preferences By Category

Updates notification preferences by category in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-notification-preferences-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-notification-preferences-by-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "communicationChannelId": "string",
  "notificationPreferencesFrequency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-notification-preferences-by-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "communicationChannelId": "string",
    "notificationPreferencesFrequency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | The Canvas notification preference category. |
| `communicationChannelId` | string | yes | The Canvas communication channel ID. |
| `notificationPreferencesFrequency` | string | yes | The desired frequency for this notification category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notification_preferences": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notification_preferences` | array<object> |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /users/self/communication_channels/:communication_channel_id/notification_preference_categories/:category` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notification-preferences-by-category.md) for the provider-specific parameters and requirements.

