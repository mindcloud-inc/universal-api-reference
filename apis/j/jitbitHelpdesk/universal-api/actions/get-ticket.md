# Jitbit Helpdesk: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": 1,
      "body": "string",
      "categoryId": 1,
      "categoryName": "Ava Chen",
      "issueDate": "string",
      "lastUpdated": "string",
      "priority": 1,
      "status": "string",
      "statusId": 1,
      "subject": "ava@example.com",
      "ticketId": 1,
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | number | Assigned technician user ID. |
| `body` | string | Ticket body. |
| `categoryId` | number | Ticket category ID. |
| `categoryName` | string | Ticket category name. |
| `issueDate` | string | Ticket creation timestamp. |
| `lastUpdated` | string | Last update timestamp. |
| `priority` | number | Ticket priority value. |
| `status` | string | Ticket status label. |
| `statusId` | number | Ticket status ID. |
| `subject` | string | Ticket subject. |
| `ticketId` | number | Ticket ID. |
| `url` | string | Ticket URL. |
| `userId` | number | Submitter user ID. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /ticket` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

