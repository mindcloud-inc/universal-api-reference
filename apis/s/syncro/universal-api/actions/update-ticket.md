# Syncro: Update Ticket

Updates an existing ticket in Syncro.

```
PUT https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Syncro ticket ID. |
| `customerId` | number | no |  |
| `ticketTypeId` | number | no |  |
| `number` | string | no |  |
| `subject` | string | yes |  |
| `dueDate` | date | no |  |
| `startAt` | date | no |  |
| `endAt` | date | no |  |
| `locationId` | number | no |  |
| `problemType` | string | no |  |
| `status` | string | no |  |
| `userId` | number | no |  |
| `properties` | object | no |  |
| `assetIds[]` | array<number> | no |  |
| `signatureName` | string | no |  |
| `signatureData` | string | no |  |
| `slaId` | number | no |  |
| `contactId` | number | no |  |
| `priority` | string | no |  |
| `outtakeFormData` | string | no |  |
| `outtakeFormDate` | date | no |  |
| `outtakeFormName` | string | no |  |
| `tagList[]` | array<string> | no |  |
| `commentsAttributes[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ticket": {
        "comments": [
          {
            "body": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": 1,
            "subject": "string"
          }
        ],
        "contact": {
          "id": 1,
          "name": "Ava Chen"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customer": {
          "businessAndFullName": "Ava Chen",
          "id": 1
        },
        "customerBusinessThenName": "Ava Chen",
        "customerId": 1,
        "dueDate": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "number": 1,
        "priority": "string",
        "problemType": "string",
        "status": "string",
        "subject": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ticket.comments[].body` | string |  |
| `ticket.comments[].createdAt` | date |  |
| `ticket.comments[].id` | number |  |
| `ticket.comments[].subject` | string |  |
| `ticket.contact.id` | number |  |
| `ticket.contact.name` | string |  |
| `ticket.createdAt` | date |  |
| `ticket.customer.businessAndFullName` | string |  |
| `ticket.customer.id` | number |  |
| `ticket.customerBusinessThenName` | string |  |
| `ticket.customerId` | number |  |
| `ticket.dueDate` | date |  |
| `ticket.id` | number |  |
| `ticket.number` | number |  |
| `ticket.priority` | string |  |
| `ticket.problemType` | string |  |
| `ticket.status` | string |  |
| `ticket.subject` | string |  |
| `ticket.updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `PUT /tickets/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

