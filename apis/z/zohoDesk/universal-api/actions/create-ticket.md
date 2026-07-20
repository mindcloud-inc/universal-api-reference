# Zoho Desk: Create Ticket



```
POST https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "departmentId": "string",
  "contactId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "departmentId": "string",
    "contactId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Subject of the new ticket. |
| `departmentId` | string | yes | Department that will own the new ticket. |
| `contactId` | string | yes | Contact who raised the new ticket. |
| `status` | string | yes | Status for the new ticket. |

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

Through the native Zoho Desk API, this operation is `POST /tickets` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

