# Agent Mail: List Inboxes

Retrieves inboxes from AgentMail for the authenticated account.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Agent Mail API, this operation is `GET /inboxes` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inboxes.md) for the provider-specific parameters and requirements.

