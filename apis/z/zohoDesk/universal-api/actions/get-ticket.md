# Zoho Desk: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | string | yes | The Zoho Desk ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "channel": "string",
      "contactId": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "departmentId": "string",
      "id": "string",
      "isArchived": true,
      "isSpam": true,
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "statusType": "string",
      "subject": "string",
      "ticketNumber": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `channel` | string |  |
| `contactId` | string |  |
| `createdTime` | date |  |
| `departmentId` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isSpam` | boolean |  |
| `modifiedTime` | date |  |
| `status` | string |  |
| `statusType` | string |  |
| `subject` | string |  |
| `ticketNumber` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /tickets/[:ticketId]` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

