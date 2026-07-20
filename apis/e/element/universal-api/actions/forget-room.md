# Element: Forget Room

Forgets a room in Element for the current user.

```
DELETE https://connect.mindcloud.co/v1/universal/element/latest/actions/forget-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/element/latest/actions/forget-room?connectionId=$CONNECTION_ID&roomId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/forget-room?${params}`, {
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
| `roomId` | string | yes | Room ID to forget. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Element API returns.

## Native endpoint

Through the native Element API, this operation is `POST /_matrix/client/v3/rooms/:roomId/forget` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forget-room.md) for the provider-specific parameters and requirements.

