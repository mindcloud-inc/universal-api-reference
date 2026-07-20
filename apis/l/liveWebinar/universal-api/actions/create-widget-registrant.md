# LiveWebinar: Create Widget Registrant

Creates a widget registrant in LiveWebinar.

```
POST https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-widget-registrant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveWebinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-widget-registrant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-widget-registrant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendConfirmation` | string | no |  |
| `widgetId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveWebinar API returns.

## Native endpoint

Through the native LiveWebinar API, this operation is `POST api/widgets/:widget_id/registrants` (base URL `https://api.archiebot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-widget-registrant.md) for the provider-specific parameters and requirements.

