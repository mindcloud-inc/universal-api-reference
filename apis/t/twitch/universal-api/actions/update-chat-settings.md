# Twitch: Update Chat Settings

Updates channel chat settings in Twitch.

```
PUT https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-chat-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-chat-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "moderatorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-chat-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "moderatorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The ID of the broadcaster whose chat settings you want to update. |
| `moderatorId` | string | yes | The ID of the moderator making the update. |
| `emoteMode` | boolean | no | Whether chat messages must contain only emotes. |
| `followerMode` | boolean | no | Whether the broadcaster restricts the chat room to followers only. |
| `followerModeDuration` | number | no | How long, in minutes, users must follow before chatting. |
| `nonModeratorChatDelay` | boolean | no | Whether to delay non-moderator messages before showing them in chat. |
| `nonModeratorChatDelayDuration` | number | no | The number of seconds to delay non-moderator chat messages. |
| `slowMode` | boolean | no | Whether to limit how often users may send messages. |
| `slowModeWaitTime` | number | no | The number of seconds users must wait between messages. |
| `subscriberMode` | boolean | no | Whether only subscribers may chat. |
| `uniqueChatMode` | boolean | no | Whether only unique chat messages are allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasterId": "string",
      "emoteMode": true,
      "followerMode": true,
      "followerModeDuration": {},
      "moderatorId": "string",
      "nonModeratorChatDelay": true,
      "nonModeratorChatDelayDuration": {},
      "slowMode": true,
      "slowModeWaitTime": {},
      "subscriberMode": true,
      "uniqueChatMode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterId` | string |  |
| `emoteMode` | boolean |  |
| `followerMode` | boolean |  |
| `followerModeDuration` | object |  |
| `moderatorId` | string |  |
| `nonModeratorChatDelay` | boolean |  |
| `nonModeratorChatDelayDuration` | object |  |
| `slowMode` | boolean |  |
| `slowModeWaitTime` | object |  |
| `subscriberMode` | boolean |  |
| `uniqueChatMode` | boolean |  |

## Native endpoint

Through the native Twitch API, this operation is `PATCH /chat/settings` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-settings.md) for the provider-specific parameters and requirements.

