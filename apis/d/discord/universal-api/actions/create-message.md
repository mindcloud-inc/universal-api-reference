# Discord: Create Message

Creates a message in a Discord channel.

```
POST https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "123456789012345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "123456789012345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel identifier. Example: `123456789012345678`. |
| `content` | string | no | Message text content. Example: `Hello from MindCloud`. |
| `tts` | boolean | no | Whether this message should use text-to-speech. Example: `false`. |
| `embeds[]` | array<object> | no | Rich embed objects for the message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedMentions` | object | no | Controls which mentions are parsed. |
| `components[]` | array<object> | no | Message components such as buttons. |
| `stickerIds[]` | array<string> | no | Sticker IDs to include with the message. |
| `attachments[]` | array<object> | no | Attachment objects for this message. |
| `messageReference` | object | no | Reference data for replies or forwards. |
| `flags` | number | no | Message flags bitfield. |
| `nonce` | string | no | Message nonce for validation. Example: `1234567890`. |
| `enforceNonce` | boolean | no | Require nonce uniqueness for this send. Example: `false`. |
| `poll` | object | no | Poll create request object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "author": {
        "avatar": "string",
        "bot": true,
        "discriminator": "string",
        "flags": 1,
        "id": "string",
        "publicFlags": 1,
        "username": "Ava Chen"
      },
      "channelId": "string",
      "components": [
        {}
      ],
      "content": "string",
      "editedTimestamp": "2026-05-07T12:00:00.000Z",
      "embeds": [
        {}
      ],
      "flags": 1,
      "id": "string",
      "mentionEveryone": true,
      "mentionRoles": [
        "string"
      ],
      "mentions": [
        {}
      ],
      "pinned": true,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "tts": true,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `author` | object |  |
| `author.avatar` | string |  |
| `author.bot` | boolean |  |
| `author.discriminator` | string |  |
| `author.flags` | number |  |
| `author.id` | string |  |
| `author.publicFlags` | number |  |
| `author.username` | string |  |
| `channelId` | string |  |
| `components` | array<object> |  |
| `content` | string |  |
| `editedTimestamp` | date |  |
| `embeds` | array<object> |  |
| `flags` | number |  |
| `id` | string |  |
| `mentionEveryone` | boolean |  |
| `mentionRoles` | array<string> |  |
| `mentions` | array<object> |  |
| `pinned` | boolean |  |
| `timestamp` | date |  |
| `tts` | boolean |  |
| `type` | number |  |

## Native endpoint

Through the native Discord API, this operation is `POST /channels/:channelId/messages` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

