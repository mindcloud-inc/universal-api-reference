# Discord-Bot: Get Reactions

Retrieves users who reacted to a Discord message.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-reactions?connectionId=$CONNECTION_ID&channelId=string&messageId=string&emojiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "messageId": "string",
  "emojiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-reactions?${params}`, {
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
| `after` | string | no | Return users after this user ID. |
| `channelId` | string | yes | Discord channel ID. |
| `messageId` | string | yes | Discord message ID. |
| `emojiName` | string | yes | URL-encoded emoji identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "bot": true,
      "global_name": "Ava Chen",
      "id": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `bot` | boolean |  |
| `global_name` | string |  |
| `id` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `GET /channels/:channelId/messages/:messageId/reactions/:emojiName` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reactions.md) for the provider-specific parameters and requirements.

