# Pusher: Terminate User Connections

Terminates a user's connections in Pusher.

```
DELETE https://connect.mindcloud.co/v1/universal/pusher/latest/actions/terminate-user-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/terminate-user-connections?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pusher/latest/actions/terminate-user-connections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The authenticated user whose active connections should be terminated. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pusher API returns.

## Native endpoint

Through the native Pusher API, this operation is `POST /apps/{{credentials.appId}}/users/:user_id/terminate_connections` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/terminate-user-connections.md) for the provider-specific parameters and requirements.

