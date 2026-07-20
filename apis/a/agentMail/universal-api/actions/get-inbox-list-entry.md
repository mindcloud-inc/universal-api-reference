# Agent Mail: Get Inbox List Entry

Retrieves an inbox list entry from a specific AgentMail inbox.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-list-entry?connectionId=$CONNECTION_ID&direction=string&entry=string&inboxId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "direction": "string",
  "entry": "string",
  "inboxId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-list-entry?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direction` | string | yes | List direction: send, receive, or reply. |
| `entry` | string | yes | Email address or domain entry. |
| `inboxId` | string | yes | The AgentMail inbox ID. |
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

Through the native Agent Mail API, this operation is `GET /inboxes/{inbox_id}/lists/{direction}/{type}/{entry}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-list-entry.md) for the provider-specific parameters and requirements.

