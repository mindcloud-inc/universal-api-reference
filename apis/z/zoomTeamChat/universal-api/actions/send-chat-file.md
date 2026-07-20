# Zoom Team Chat: Send Chat File



```
POST https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "me"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/send-chat-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "me"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The user's ID. Default: `me`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "file_name": "Ava Chen",
      "file_size": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string |  |
| `file_name` | string |  |
| `file_size` | number |  |
| `id` | string |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `POST https://file.zoom.us/v2/chat/users/:userId/messages/files` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-file.md) for the provider-specific parameters and requirements.

