# Agent Mail: Create Inbox

Creates a new inbox in AgentMail.

```
POST https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | Client-provided idempotency ID. |
| `displayName` | string | no | Display name for the new inbox. |
| `domain` | string | no | Domain for the new inbox. |
| `username` | string | no | Username for the new inbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "inbox_id": "string",
      "pod_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string | Client ID of the inbox. |
| `created_at` | date | Creation timestamp. |
| `display_name` | string | Display name for the inbox. |
| `email` | string | Inbox email address. |
| `inbox_id` | string | The ID of the inbox. |
| `pod_id` | string | ID of the pod. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `POST /inboxes` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox.md) for the provider-specific parameters and requirements.

