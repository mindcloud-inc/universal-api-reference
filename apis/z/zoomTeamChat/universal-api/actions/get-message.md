# Zoom Team Chat: Get Message



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-message?connectionId=$CONNECTION_ID&userId=me&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "me",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | The unique identifier of the message. |
| `toContact` | string | no | The recipient contact email, member ID, or user ID. |
| `toChannel` | string | no | The channel ID where the message was sent. |
| `downloadFileFormats` | string | no | Requested file download format. |

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

Through the native Zoom Team Chat API, this operation is `GET /chat/users/:userId/messages/:messageId` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

