# Zulip: Remove Emoji Reaction

Removes an emoji reaction from a Zulip message.

```
DELETE https://connect.mindcloud.co/v1/universal/zulip/latest/actions/remove-emoji-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/remove-emoji-reaction?connectionId=$CONNECTION_ID&emojiName=Ava%20Chen&messageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emojiName": "Ava Chen",
  "messageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/remove-emoji-reaction?${params}`, {
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
| `emojiName` | string | yes | The emoji name to remove from the message. |
| `messageId` | number | yes | The target message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `DELETE /messages/:message_id/reactions` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-emoji-reaction.md) for the provider-specific parameters and requirements.

