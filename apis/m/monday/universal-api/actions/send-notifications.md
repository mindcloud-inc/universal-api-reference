# Monday: Send Notifications

Sends a notification to a user in Monday.

```
POST https://connect.mindcloud.co/v1/universal/monday/latest/actions/send-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monday/latest/actions/send-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monday/latest/actions/send-notifications', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no |  |
| `userId` | string | no |  |
| `targetId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Monday API returns.

## Native endpoint

Through the native Monday API, this operation is `POST` (base URL `https://api.monday.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notifications.md) for the provider-specific parameters and requirements.

