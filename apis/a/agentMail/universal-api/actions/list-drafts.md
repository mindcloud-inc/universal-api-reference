# Agent Mail: List Drafts

Retrieves drafts from AgentMail for the authenticated account.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-drafts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-drafts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-drafts?${params}`, {
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
      "attachments": [
        {}
      ],
      "draft_id": "string",
      "inbox_id": "string",
      "labels": [
        "string"
      ],
      "preview": "string",
      "send_at": "2026-05-07T12:00:00.000Z",
      "send_status": "string",
      "subject": "string",
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
| `attachments` | array<object> | Draft attachments. |
| `draft_id` | string | ID of the draft. |
| `inbox_id` | string | The ID of the inbox. |
| `labels` | array<string> | Labels on the draft. |
| `preview` | string | Draft text preview. |
| `send_at` | date | Scheduled send timestamp. |
| `send_status` | string | Scheduled send status of the draft. |
| `subject` | string | Draft subject. |
| `to` | array<string> | Draft recipient addresses. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /drafts` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-drafts.md) for the provider-specific parameters and requirements.

