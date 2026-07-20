# Zoho Desk: Search Tickets



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tickets?${params}`, {
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
| `id` | string | no | Search for an exact Zoho Desk ticket ID. |
| `departmentId` | list<number> | no |  |
| `channel` | list<string> | no |  |
| `createdTimeRange` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "modifiedTime": "string",
      "subCategory": {},
      "statusType": "string",
      "subject": "string",
      "dueDate": {},
      "departmentId": "string",
      "channel": "string",
      "onholdTime": {},
      "language": {},
      "resolution": {},
      "closedTime": {},
      "isOverDue": true,
      "contact": {
        "lastName": "Chen",
        "firstName": "Ava",
        "phone": {},
        "mobile": {},
        "id": "string",
        "type": {},
        "email": "ava@example.com",
        "account": {}
      },
      "createdTime": "string",
      "customerResponseTime": "string",
      "productId": {},
      "contactId": "string",
      "threadCount": "string",
      "priority": {},
      "classification": {},
      "commentCount": "string",
      "accountId": {},
      "phone": {},
      "webUrl": "https://example.com",
      "assignee": {},
      "isSpam": true,
      "childTicketCount": "string",
      "status": "string",
      "ticketNumber": "string",
      "isArchived": true,
      "isRead": true,
      "description": {},
      "responseDueDate": {},
      "modifiedBy": "string",
      "department": {
        "name": "Ava Chen",
        "id": "string"
      },
      "email": {},
      "product": {},
      "slaId": {},
      "relationshipType": "string",
      "lastThread": {},
      "team": {},
      "layoutId": "string",
      "assigneeId": {},
      "createdBy": "string",
      "teamId": {},
      "isEscalated": true,
      "category": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `modifiedTime` | string |  |
| `subCategory` | object |  |
| `statusType` | string |  |
| `subject` | string |  |
| `dueDate` | object |  |
| `departmentId` | string |  |
| `channel` | string |  |
| `onholdTime` | object |  |
| `language` | object |  |
| `resolution` | object |  |
| `closedTime` | object |  |
| `isOverDue` | boolean |  |
| `contact.lastName` | string |  |
| `contact.firstName` | string |  |
| `contact.phone` | object |  |
| `contact.mobile` | object |  |
| `contact.id` | string |  |
| `contact.type` | object |  |
| `contact.email` | string |  |
| `contact.account` | object |  |
| `createdTime` | string |  |
| `customerResponseTime` | string |  |
| `productId` | object |  |
| `contactId` | string |  |
| `threadCount` | string |  |
| `priority` | object |  |
| `classification` | object |  |
| `commentCount` | string |  |
| `accountId` | object |  |
| `phone` | object |  |
| `webUrl` | string |  |
| `assignee` | object |  |
| `isSpam` | boolean |  |
| `childTicketCount` | string |  |
| `status` | string |  |
| `ticketNumber` | string |  |
| `isArchived` | boolean |  |
| `isRead` | boolean |  |
| `description` | object |  |
| `responseDueDate` | object |  |
| `modifiedBy` | string |  |
| `department.name` | string |  |
| `department.id` | string |  |
| `email` | object |  |
| `product` | object |  |
| `slaId` | object |  |
| `relationshipType` | string |  |
| `lastThread` | object |  |
| `team` | object |  |
| `layoutId` | string |  |
| `assigneeId` | object |  |
| `createdBy` | string |  |
| `teamId` | object |  |
| `isEscalated` | boolean |  |
| `category` | object |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /tickets/search` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

