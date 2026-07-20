# Agent Mail: Create Inbox List Entry

Creates an inbox list entry in a specific AgentMail inbox.

```
POST https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox-list-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "direction": "string",
  "entry": "string",
  "inboxId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox-list-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "direction": "string",
    "entry": "string",
    "inboxId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direction` | string | yes | List direction: send, receive, or reply. |
| `entry` | string | yes | Email address or domain entry to add. |
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `reason` | string | no | Optional reason for the list entry. |
| `type` | string | yes | List type: allow or block. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "entry": "ava@example.com",
      "entry_type": "string",
      "inbox_id": "string",
      "list_type": "string",
      "organization_id": "string",
      "pod_id": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `direction` | string | Direction of the list entry. |
| `entry` | string | Email address or domain for the list entry. |
| `entry_type` | string | Email or domain entry type. |
| `inbox_id` | string | ID of the inbox. |
| `list_type` | string | Allow or block list type. |
| `organization_id` | string | ID of the organization. |
| `pod_id` | string | ID of the pod. |
| `reason` | string | Reason for the entry. |

## Native endpoint

Through the native Agent Mail API, this operation is `POST /inboxes/{inbox_id}/lists/{direction}/{type}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox-list-entry.md) for the provider-specific parameters and requirements.

