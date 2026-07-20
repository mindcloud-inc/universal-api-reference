# Basecamp: Create Message

Creates a new message on a Basecamp message board.

```
POST https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "195539477",
  "boardId": "1069479392",
  "subject": "Kickoff"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "195539477",
    "boardId": "1069479392",
    "subject": "Kickoff"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Example: `195539477`. |
| `boardId` | number | yes | Example: `1069479392`. |
| `subject` | string | yes | Example: `Kickoff`. |
| `content` | string | no | Example: `<div><strong>Welcome to Basecamp, everyone.</strong></div>`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | number | no |  |
| `subscriptions[]` | array<number> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `POST /:accountId/message_boards/:boardId/messages.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

