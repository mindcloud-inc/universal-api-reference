# Zeplin: Update User Notification Settings

Updates user notification settings in Zeplin.

```
PUT https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-user-notification-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-user-notification-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "isRead": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-user-notification-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "isRead": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type[]` | array<string> | no | Filter by type Example: `?type=project.extension&type=styleguide.extension` |
| `id[]` | array<string> | no | Filter by id Example: `?id=5fbe387f8c72ef23659fb500&id=602281f4783f72fccc045484` |
| `isRead` | boolean | yes | New is_read status for notifications |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `PATCH /users/me/notifications` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-notification-settings.md) for the provider-specific parameters and requirements.

