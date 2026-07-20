# Jitbit Helpdesk: Get Parent Ticket



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-parent-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-parent-ticket?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-parent-ticket?${params}`, {
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
| `id` | number | yes | Jitbit child ticket ID. |
| `returnFullTicket` | boolean | no | Set true to return the full parent ticket object instead of only the parent ticket ID. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "issueDate": "string",
      "lastUpdated": "string",
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
| `categoryId` | number | Parent ticket category ID. |
| `issueDate` | string | Parent ticket creation timestamp. |
| `lastUpdated` | string | Parent ticket last update timestamp. |
| `status` | string | Parent ticket status label. |
| `statusId` | number | Parent ticket status ID. |
| `subject` | string | Parent ticket subject. |
| `ticketId` | number | Parent ticket ID. |
| `url` | string | Parent ticket URL. |
| `userId` | number | Submitter user ID. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /ParentTicket` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parent-ticket.md) for the provider-specific parameters and requirements.

