# Freshdesk: Create Ticket

Creates a new ticket in Freshdesk.

```
POST https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the requester |
| `requesterId` | list<number> | no | User ID of the requester |
| `email` | string | no | Email address of the requester |
| `facebookId` | string | no | Facebook ID of the requester |
| `phone` | string | no | Phone number of the requester |
| `twitterId` | string | no | Twitter handle of the requester |
| `uniqueExternalId` | string | no | External ID of the requester |
| `subject` | string | no | Subject of the ticket |
| `type` | string | no | Ticket type/category |
| `status` | number | no | Status of the ticket |
| `priority` | number | no | Priority of the ticket |
| `description` | string | no | HTML content of the ticket |
| `responderId` | list<number> | no | ID of the assigned agent |
| `attachments[]` | array<object> | no | Ticket attachments |
| `ccEmails[]` | array<string> | no | Email addresses added in CC |
| `customFields` | object | no | Key-value pairs for custom ticket fields |
| `dueBy` | date | no | SLA due date/time for the ticket |
| `emailConfigId` | number | no | Email configuration ID for the ticket |
| `frDueBy` | date | no | First response due date/time |
| `groupId` | number | no | Group ID assigned to the ticket |
| `parentId` | list<number> | no | Parent ticket ID for child-ticket linking |
| `productId` | number | no | Product ID associated with the ticket |
| `source` | number | no | Source channel through which the ticket was created |
| `tags[]` | array<string> | no | Tags associated with the ticket |
| `companyId` | list<number> | no | Company ID of the requester |
| `internalAgentId` | list<number> | no | Internal agent ID to assign |
| `internalGroupId` | number | no | Internal group ID to assign |
| `lookupParameter` | string | no | Lookup field value for custom object linkage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdAt": "string",
      "dueBy": "string",
      "frDueBy": "string",
      "id": 1,
      "priority": 1,
      "requesterId": 1,
      "source": 1,
      "status": 1,
      "subject": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdAt` | string |  |
| `dueBy` | string |  |
| `frDueBy` | string |  |
| `id` | number |  |
| `priority` | number |  |
| `requesterId` | number |  |
| `source` | number |  |
| `status` | number |  |
| `subject` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `POST /tickets` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

