# LiveWebinar: Enable User

Enables a user in LiveWebinar.

```
PUT https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/enable-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveWebinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/enable-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/enable-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveWebinar API returns.

## Native endpoint

Through the native LiveWebinar API, this operation is `PUT api/users/:user_id/enable` (base URL `https://api.archiebot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-user.md) for the provider-specific parameters and requirements.

