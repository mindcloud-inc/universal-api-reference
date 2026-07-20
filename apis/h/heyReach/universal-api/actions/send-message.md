# Hey Reach: Send Message

Sends a message to a LinkedIn conversation in Hey Reach.

```
POST https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "conversationId": "string",
  "linkedInAccountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "conversationId": "string",
    "linkedInAccountId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes |  |
| `subject` | string | no |  |
| `conversationId` | string | yes |  |
| `linkedInAccountId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hey Reach API returns.

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/inbox/SendMessage` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

