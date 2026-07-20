# Noor: Send Message

Creates a message in a Noor thread.

```
POST https://connect.mindcloud.co/v1/universal/noor/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Noor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/noor/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "thread": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noor/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "thread": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Get this from Noor Settings > API. |
| `thread` | string | yes | Enter the exact Noor thread name. |
| `text` | string | yes | The message text. Markdown is supported. |
| `documentId` | string | no | Optional attached file ID uploaded with Noor's upload API. |
| `notifyByName[]` | array<string> | no | Optional Noor member names to notify, for example ["Ben"]. |
| `notifyById[]` | array<string> | no | Optional Noor member IDs to notify, for example ["User:123a"]. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Noor API returns.

## Native endpoint

Through the native Noor API, this operation is `POST /sendMessage` (base URL `https://sun.noor.to/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

