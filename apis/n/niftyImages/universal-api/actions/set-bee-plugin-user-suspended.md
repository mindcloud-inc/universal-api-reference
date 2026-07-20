# NiftyImages: Set Bee Plugin User Suspended

Updates a Bee Plugin user suspension in NiftyImages.

```
PUT https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/set-bee-plugin-user-suspended
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/set-bee-plugin-user-suspended" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pluginKey": "string",
  "user": "string",
  "suspended": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/set-bee-plugin-user-suspended', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pluginKey": "string",
    "user": "string",
    "suspended": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pluginKey` | string | yes | Bee Plugin key. |
| `user` | string | yes | User identifier. |
| `suspended` | boolean | yes | Set to true to suspend the user, or false to unsuspend the user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NiftyImages API returns.

## Native endpoint

Through the native NiftyImages API, this operation is `PUT /BeePlugin/:pluginKey/Users/:user` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-bee-plugin-user-suspended.md) for the provider-specific parameters and requirements.

