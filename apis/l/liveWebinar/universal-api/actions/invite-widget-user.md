# LiveWebinar: Invite Widget User

Invites a user to a widget in LiveWebinar.

```
POST https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/invite-widget-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveWebinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/invite-widget-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/invite-widget-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `role` | string | no |  |
| `widgetId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveWebinar API returns.

## Native endpoint

Through the native LiveWebinar API, this operation is `POST api/widgets/:widget_id/invites/invite` (base URL `https://api.archiebot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-widget-user.md) for the provider-specific parameters and requirements.

