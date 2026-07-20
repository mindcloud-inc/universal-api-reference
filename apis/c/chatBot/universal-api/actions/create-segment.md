# ChatBot: Create Segment

Creates a new user segment in ChatBot.

```
POST https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Test Segment 2026-03-18"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Test Segment 2026-03-18"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Segment name. Example: `Codex Test Segment 2026-03-18`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created segment identifier. |
| `status` | object | Mutation status payload returned by ChatBot. |
| `timestamp` | date | Timestamp returned by ChatBot for the mutation. |

## Native endpoint

Through the native ChatBot API, this operation is `POST /users/segments` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

