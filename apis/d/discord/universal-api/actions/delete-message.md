# Discord: Delete Message

Deletes a message from a Discord channel.

```
DELETE https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-message?connectionId=$CONNECTION_ID&channelId=123456789012345678&messageId=123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "123456789012345678",
  "messageId": "123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/delete-message?${params}`, {
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
| `channelId` | string | yes | Channel identifier. Example: `123456789012345678`. |
| `messageId` | string | yes | Message identifier. Example: `123456789012345678`. |

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

Through the native Discord API, this operation is `DELETE /channels/:channelId/messages/:messageId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

