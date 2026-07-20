# Agent Mail: Send Inbox Draft

Sends a draft from a specific AgentMail inbox.

```
POST https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/send-inbox-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/send-inbox-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftId": "string",
  "inboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/send-inbox-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftId": "string",
    "inboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftId` | string | yes | The AgentMail draft ID. |
| `inboxId` | string | yes | The AgentMail inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "thread_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string | ID of the sent message. |
| `thread_id` | string | ID of the thread containing the sent draft. |

## Native endpoint

Through the native Agent Mail API, this operation is `POST /inboxes/{inbox_id}/drafts/{draft_id}/send` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-inbox-draft.md) for the provider-specific parameters and requirements.

