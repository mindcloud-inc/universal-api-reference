# Zoho Cliq: Update Channel

Updates an existing channel in Zoho Cliq.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The ID of the channel to update. |
| `name` | string | no | The updated channel name. |
| `description` | string | no | The updated channel description. |
| `imageData` | string | no | The updated base64-encoded display image for the channel. |
| `config.replyMode` | string | no | How replies should work in the channel: normal_reply, threads, or both. |
| `config.leaveJoinInfo` | string | no | Whether join and leave events should be posted in the channel. |
| `config.addRemoveInfo` | string | no | Whether add and remove participant events should be posted in the channel. |
| `config.meetingChatType` | string | no | Where meeting messages should be posted: channel, thread, or host_choice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_id": "string",
      "chat_id": "string",
      "creation_time": "string",
      "description": "string",
      "invite_only": true,
      "joined": true,
      "last_modified_time": "string",
      "level": "string",
      "name": "Ava Chen",
      "participant_count": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_id` | string | The channel identifier. |
| `chat_id` | string | The backing chat identifier. |
| `creation_time` | string | The channel creation time. |
| `description` | string | The channel description. |
| `invite_only` | boolean | Whether the channel is invite only. |
| `joined` | boolean | Whether the authenticated user is joined. |
| `last_modified_time` | string | The channel last modified time. |
| `level` | string | The channel level. |
| `name` | string | The channel name. |
| `participant_count` | number | The participant count. |
| `status` | string | The channel status. |

## Native endpoint

Through the native Zoho Cliq API, this operation is `PUT /channels/:channelId` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

