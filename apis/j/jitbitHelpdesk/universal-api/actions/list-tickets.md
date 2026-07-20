# Jitbit Helpdesk: List Tickets



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-tickets?${params}`, {
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
| `mode` | string | no | Which ticket bucket to return: all, unanswered, unclosed, or handledbyme. One of: `0`, `1`, `2`, `3`. Example: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": 1,
      "categoryId": 1,
      "companyId": 1,
      "email": "ava@example.com",
      "issueDate": "string",
      "issueId": 1,
      "lastUpdated": "string",
      "priority": 1,
      "status": "string",
      "statusId": 1,
      "subject": "ava@example.com",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | number | Assigned technician user ID. |
| `categoryId` | number | Ticket category ID. |
| `companyId` | number | Requester company ID when present. |
| `email` | string | Requester email address. |
| `issueDate` | string | Ticket creation timestamp. |
| `issueId` | number | Ticket issue ID. |
| `lastUpdated` | string | Last update timestamp. |
| `priority` | number | Ticket priority value. |
| `status` | string | Ticket status label. |
| `statusId` | number | Ticket status ID. |
| `subject` | string | Ticket subject line. |
| `userName` | string | Requester username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /Tickets` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

