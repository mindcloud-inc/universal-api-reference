# Pinghome: Update Team Notification Channel Status

Updates team notification channel status in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-team-notification-channel-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-team-notification-channel-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "enabled": true,
  "priority": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-team-notification-channel-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "enabled": true,
    "priority": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the team. |
| `enabled` | boolean | yes | Boolean value indicating whether the notification channel is enabled or disabled. |
| `priority` | number | yes | The priority number of the notification channel to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /customer-cmd/v1/team/:id/notification-channel/enabled` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-notification-channel-status.md) for the provider-specific parameters and requirements.

