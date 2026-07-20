# Dashly: Set User Presence

Sends a heartbeat signal for a Dashly user.

```
PUT https://connect.mindcloud.co/v1/universal/dashly/latest/actions/set-user-presence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/set-user-presence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "presence": "online"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashly/latest/actions/set-user-presence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "presence": "online"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `presence` | string | yes | Default: `online`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentPage` | string | no |  |
| `currentUrl` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dashly API returns.

## Native endpoint

Through the native Dashly API, this operation is `POST users/:id/setpresence` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-presence.md) for the provider-specific parameters and requirements.

