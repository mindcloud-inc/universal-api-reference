# Discord: Delete Own Reaction

Deletes the current user's reaction from a Discord message.

```
DELETE https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-own-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-own-reaction?connectionId=$CONNECTION_ID&channelId=string&messageId=string&emojiName=party_parrot%253A123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "messageId": "string",
  "emojiName": "party_parrot%3A123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-own-reaction?${params}`, {
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
| `channelId` | string | yes | ID of the channel containing the message. |
| `messageId` | string | yes | ID of the message to remove reaction from. |
| `emojiName` | string | yes | Emoji to remove (URL-encoded as required by Discord). Example: `party_parrot%3A123456789012345678`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body on success. |

## Native endpoint

Through the native Discord API, this operation is `DELETE /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-own-reaction.md) for the provider-specific parameters and requirements.

