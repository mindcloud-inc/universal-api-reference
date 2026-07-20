# Agent Mail: Update Inbox Draft

Updates a draft in a specific AgentMail inbox.

```
PUT https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftId": "string",
  "inboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/update-inbox-draft', {
  method: 'PUT',
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
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "draft_id": "string",
      "html": "string",
      "inbox_id": "string",
      "labels": [
        "string"
      ],
      "preview": "string",
      "send_at": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "text": "string",
      "to": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string | Client ID of the draft. |
| `created_at` | date | Creation timestamp. |
| `draft_id` | string | ID of the draft. |
| `html` | string | HTML body. |
| `inbox_id` | string | The ID of the inbox. |
| `labels` | array<string> | Labels on the draft. |
| `preview` | string | Draft text preview. |
| `send_at` | date | Scheduled send timestamp. |
| `subject` | string | Draft subject. |
| `text` | string | Plain text body. |
| `to` | array<string> | Draft recipient addresses. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `PATCH /inboxes/{inbox_id}/drafts/{draft_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbox-draft.md) for the provider-specific parameters and requirements.

