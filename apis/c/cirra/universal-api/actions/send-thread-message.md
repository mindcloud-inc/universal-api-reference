# Cirra: Send Thread Message

Adds a message to a Cirra thread and starts a run.

```
POST https://connect.mindcloud.co/v1/universal/cirra/latest/actions/send-thread-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/send-thread-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string",
  "content": "Draft a concise update for the customer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/send-thread-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string",
    "content": "Draft a concise update for the customer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | list | yes | The thread ID. |
| `content` | string | yes | The message content to append to the thread. Example: `Draft a concise update for the customer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "runId": "string",
      "status": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `runId` | string |  |
| `status` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Cirra API, this operation is `POST /v1/cirra/threads/:threadId/messages` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-thread-message.md) for the provider-specific parameters and requirements.

