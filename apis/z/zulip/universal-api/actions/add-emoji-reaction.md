# Zulip: Add Emoji Reaction

Adds an emoji reaction to a Zulip message.

```
PUT https://connect.mindcloud.co/v1/universal/zulip/latest/actions/add-emoji-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/add-emoji-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emojiName": "Ava Chen",
  "messageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zulip/latest/actions/add-emoji-reaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emojiName": "Ava Chen",
    "messageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emojiName` | string | yes | The emoji name to add as a reaction. |
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

Through the native Zulip API, this operation is `POST /messages/:message_id/reactions` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-emoji-reaction.md) for the provider-specific parameters and requirements.

