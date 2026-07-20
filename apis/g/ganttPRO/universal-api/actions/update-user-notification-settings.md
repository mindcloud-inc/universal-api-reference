# GanttPRO: Update User Notification Settings

Updates notification settings for a GanttPRO user.

```
PUT https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-user-notification-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-user-notification-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "envType": "0",
  "actionType": "0",
  "active": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-user-notification-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "envType": "0",
    "actionType": "0",
    "active": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | GanttPRO user identifier. |
| `envType` | string | yes | Notification channel: email, desktop, or mobile. One of: `0`, `1`, `2`. |
| `actionType` | string | yes | Notification event type such as mention, assign, comment, attachment, task_start, deadline, team_invite, or task_end. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `active` | number | yes | Use 1 to enable the notification or 0 to disable it. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `PUT /users/:userId/notification` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-notification-settings.md) for the provider-specific parameters and requirements.

