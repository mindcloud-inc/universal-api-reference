# Stream: Upsert Users

Creates or updates users in Stream.

```
PUT https://connect.mindcloud.co/v1/universal/stream/latest/actions/upsert-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stream/latest/actions/upsert-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stream/latest/actions/upsert-users', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `users` | object | yes | Map of user IDs to user objects to upsert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "membershipDeletionTaskId": "string",
      "users": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |
| `membershipDeletionTaskId` | string |  |
| `users` | object |  |

## Native endpoint

Through the native Stream API, this operation is `POST /users` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-users.md) for the provider-specific parameters and requirements.

