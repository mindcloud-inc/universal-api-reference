# Zulip: Edit Message

Updates an existing message in Zulip.

```
PUT https://connect.mindcloud.co/v1/universal/zulip/latest/actions/edit-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/edit-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zulip/latest/actions/edit-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Updated Markdown content for the message. |
| `messageId` | number | yes | The target message ID. |
| `topic` | string | no | The new topic for the message thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detached_uploads": [
        "string"
      ],
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
| `detached_uploads` | array |  |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `PATCH /messages/:message_id` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-message.md) for the provider-specific parameters and requirements.

