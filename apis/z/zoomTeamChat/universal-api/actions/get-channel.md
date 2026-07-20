# Zoom Team Chat: Get Channel



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-channel?connectionId=$CONNECTION_ID&userId=me&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "me",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/get-channel?${params}`, {
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
| `userId` | string | yes | The unique identifier of the user who is the member of the channel. Default: `me`. |
| `channelId` | string | yes | The channel's unique identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_settings": {},
      "channel_url": "https://example.com",
      "id": "string",
      "jid": "string",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_settings` | object |  |
| `channel_url` | string |  |
| `id` | string |  |
| `jid` | string |  |
| `name` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/users/:userId/channels/:channelId` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

