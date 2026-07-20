# Zendesk: Execute View

Retrieves results for a Zendesk view.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/execute-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/execute-view?connectionId=$CONNECTION_ID&limit=25&offset=0&view_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "view_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/execute-view?${params}`, {
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
| `view_id` | number | yes | View ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "groupId": 1,
      "id": 1,
      "isPublic": true,
      "organizationId": 1,
      "priority": "string",
      "requesterId": 1,
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number | Assignee user id. |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Ticket description. |
| `groupId` | number | Group id attached to the ticket. |
| `id` | number | Ticket id. |
| `isPublic` | boolean | Whether the ticket is public. |
| `organizationId` | number | Organization id attached to the ticket. |
| `priority` | string | Ticket priority. |
| `requesterId` | number | Requester user id. |
| `status` | string | Ticket status. |
| `subject` | string | Ticket subject. |
| `tags[]` | string | Tags attached to the ticket. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the ticket resource. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /views/:view_id/execute.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/execute-view.md) for the provider-specific parameters and requirements.

