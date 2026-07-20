# Agent Mail: Update Inbox Thread

Updates a thread in a specific AgentMail inbox.

```
PUT https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "threadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `threadId` | string | yes | The AgentMail thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "labels": [
        "string"
      ],
      "thread_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labels` | array<string> | Labels on the thread. |
| `thread_id` | string | ID of the thread. |

## Native endpoint

Through the native Agent Mail API, this operation is `PATCH /inboxes/{inbox_id}/threads/{thread_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbox-thread.md) for the provider-specific parameters and requirements.

