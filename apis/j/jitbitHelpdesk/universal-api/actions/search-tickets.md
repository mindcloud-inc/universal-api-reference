# Jitbit Helpdesk: Search Tickets



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/search-tickets?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/search-tickets?${params}`, {
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
| `query` | string | yes | Search text for Jitbit ticket search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": 1,
      "category": "string",
      "categoryId": 1,
      "issueDate": "string",
      "issueId": 1,
      "lastUpdated": "string",
      "priority": 1,
      "status": "string",
      "statusId": 1,
      "subject": "ava@example.com",
      "userId": 1,
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
| `category` | string | Category name. |
| `categoryId` | number | Category ID. |
| `issueDate` | string | Ticket creation timestamp. |
| `issueId` | number | Ticket issue ID. |
| `lastUpdated` | string | Last update timestamp. |
| `priority` | number | Ticket priority. |
| `status` | string | Ticket status label. |
| `statusId` | number | Ticket status ID. |
| `subject` | string | Ticket subject. |
| `userId` | number | Requester user ID. |
| `userName` | string | Requester username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /Search` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

