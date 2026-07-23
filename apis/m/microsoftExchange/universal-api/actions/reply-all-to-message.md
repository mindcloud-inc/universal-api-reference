# Microsoft Exchange: Reply All to Message

Replies to all recipients of a message in Microsoft Exchange.

```
POST https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/reply-all-to-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/reply-all-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/reply-all-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The ID of the Exchange message to reply-all to. Example: `AAMkAG...`. |
| `comment` | string | no | Optional text to include in the reply-all. Example: `Thanks everyone - this is a reply-all test from the MindCloud Microsoft Exchange app.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Exchange API returns.

## Native endpoint

Through the native Microsoft Exchange API, this operation is `POST /v1.0/me/messages/{{messageId}}/replyAll` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-all-to-message.md) for the provider-specific parameters and requirements.

