# Jitbit Helpdesk: List Linked Tickets



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-linked-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-linked-tickets?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-linked-tickets?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID to list linked tickets for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "issueDate": "string",
      "lastName": "Chen",
      "statusId": 1,
      "subject": "ava@example.com",
      "ticketId": 1,
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string | Requester first name. |
| `issueDate` | string | Linked ticket creation timestamp. |
| `lastName` | string | Requester last name. |
| `statusId` | number | Linked ticket status ID. |
| `subject` | string | Linked ticket subject. |
| `ticketId` | number | Linked ticket ID. |
| `userId` | number | Requester user ID. |
| `username` | string | Requester username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /LinkedTickets` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linked-tickets.md) for the provider-specific parameters and requirements.

