# Channels: Disable User

Disables a user in Channels.

```
PUT https://connect.mindcloud.co/v1/universal/channels/latest/actions/disable-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channels/latest/actions/disable-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/disable-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | User ID to disable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "role": "string",
      "state": "string",
      "surname": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `role` | string |  |
| `state` | string |  |
| `surname` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Channels API, this operation is `PUT /api/v1/users/{userId}/disable` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-user.md) for the provider-specific parameters and requirements.

