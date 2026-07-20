# Zoom Team Chat: List User's Chat Sessions



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=me" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "me"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-sessions?${params}`, {
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
| `userId` | string | yes | The user ID of the sessions being queried. Default: `me`. |
| `type` | string | no | The session type to query. |
| `searchStar` | boolean | no | Search only starred chats. |
| `from` | string | no | The start timestamp in ISO-8601 format. |
| `to` | string | no | The end timestamp in ISO-8601 format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoom Team Chat API returns.

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/users/:userId/sessions` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users-chat-sessions.md) for the provider-specific parameters and requirements.

