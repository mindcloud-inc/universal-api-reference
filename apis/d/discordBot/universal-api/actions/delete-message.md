# Discord-Bot: Delete Message

Deletes a message from a Discord channel.

```
DELETE https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-message?connectionId=$CONNECTION_ID&channelId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-message?${params}`, {
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
| `channelId` | string | yes | Discord channel ID. |
| `messageId` | string | yes | Discord message ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Discord-Bot API returns.

## Native endpoint

Through the native Discord-Bot API, this operation is `DELETE /channels/:channelId/messages/:messageId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

