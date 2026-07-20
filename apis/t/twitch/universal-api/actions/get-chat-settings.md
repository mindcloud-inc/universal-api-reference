# Twitch: Get Chat Settings

Retrieves channel chat settings from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-chat-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-chat-settings?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-chat-settings?${params}`, {
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
| `broadcasterId` | string | yes | The ID of the broadcaster whose chat settings you want to get. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moderatorId` | string | no | The ID of a moderator in the broadcaster’s channel. Include this only when you need the non-moderator chat delay fields. |

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
| `slowMode` | boolean |  |
| `slowModeWaitTime` | object |  |
| `subscriberMode` | boolean |  |
| `uniqueChatMode` | boolean |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /chat/settings` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-settings.md) for the provider-specific parameters and requirements.

