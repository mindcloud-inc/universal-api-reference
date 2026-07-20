# Zoom Team Chat: List User's Chat Messages



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=me" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "me"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-users-chat-messages?${params}`, {
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
| `userId` | string | yes | The unique identifier of the user. Default: `me`. |
| `toContact` | string | no | Query messages for a specific contact. |
| `toChannel` | string | no | Query messages for a specific channel. |
| `date` | string | no | Query date in YYYY-MM-DD format. |
| `from` | string | no | Start timestamp in ISO-8601 format. |
| `to` | string | no | End timestamp in ISO-8601 format. |
| `searchType` | string | no | Search scope such as message or file. |
| `searchKey` | string | no | Search text for message or file content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_time": "string",
      "id": "string",
      "message": "string",
      "sender": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_time` | string |  |
| `id` | string |  |
| `message` | string |  |
| `sender` | object |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/users/:userId/messages` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users-chat-messages.md) for the provider-specific parameters and requirements.

