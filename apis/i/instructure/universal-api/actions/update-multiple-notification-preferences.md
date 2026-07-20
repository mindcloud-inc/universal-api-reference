# Instructure: Update Multiple Notification Preferences

Updates multiple notification preferences in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-multiple-notification-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-multiple-notification-preferences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "communicationChannelId": "string",
  "notificationPreferences": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-multiple-notification-preferences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "communicationChannelId": "string",
    "notificationPreferences": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `communicationChannelId` | string | yes | The Canvas communication channel ID. |
| `notificationPreferences` | object | yes | Object map of notification codes to preference payloads, for example { "assignment_changed": { "frequency": "never" } }. |

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

Through the native Instructure API, this operation is `PUT /users/self/communication_channels/:communication_channel_id/notification_preferences` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-notification-preferences.md) for the provider-specific parameters and requirements.

