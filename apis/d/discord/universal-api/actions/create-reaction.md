# Discord: Create Reaction

Creates a reaction on a Discord message.

```
POST https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "messageId": "string",
  "emojiName": "party_parrot%3A123456789012345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "messageId": "string",
    "emojiName": "party_parrot%3A123456789012345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | ID of the channel containing the message. |
| `messageId` | string | yes | ID of the message to react to. |
| `emojiName` | string | yes | Emoji to add as reaction (URL-encoded as required by Discord). Example: `party_parrot%3A123456789012345678`. |

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

Through the native Discord API, this operation is `PUT /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reaction.md) for the provider-specific parameters and requirements.

