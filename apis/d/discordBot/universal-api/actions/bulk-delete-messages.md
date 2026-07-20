# Discord-Bot: Bulk Delete Messages

Deletes multiple messages from a Discord channel.

```
DELETE https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/bulk-delete-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/bulk-delete-messages?connectionId=$CONNECTION_ID&channelId=string&messages%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "messages[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/bulk-delete-messages?${params}`, {
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
| `messages[]` | array<string> | yes | Message IDs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Discord-Bot API returns.

## Native endpoint

Through the native Discord-Bot API, this operation is `POST /channels/:channelId/messages/bulk-delete` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-messages.md) for the provider-specific parameters and requirements.

