# Zoom Team Chat: Retrieve Thread



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/retrieve-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/retrieve-thread?connectionId=$CONNECTION_ID&userId=me&messageId=string&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "me",
  "messageId": "string",
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/retrieve-thread?${params}`, {
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
| `messageId` | string | yes | The unique identifier of the main message. |
| `toChannel` | string | no | The channel ID for the thread. |
| `toContact` | string | no | The contact email, member ID, or user ID for the thread. |
| `from` | string | yes | The start timestamp of replies in ISO-8601 format. |
| `to` | string | no | The end timestamp of replies in ISO-8601 format. |
| `sort` | string | no | Sort order, such as desc or asc. |

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

Through the native Zoom Team Chat API, this operation is `GET /chat/users/:userId/messages/:messageId/thread` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-thread.md) for the provider-specific parameters and requirements.

