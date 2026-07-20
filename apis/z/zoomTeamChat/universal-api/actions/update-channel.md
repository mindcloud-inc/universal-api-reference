# Zoom Team Chat: Update Channel



```
PUT https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "me",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "me",
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The unique identifier of the user. Default: `me`. |
| `channelId` | string | yes | The channel ID. |
| `name` | string | no | The updated channel name. |

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

Through the native Zoom Team Chat API, this operation is `PATCH /chat/users/:userId/channels/:channelId` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

