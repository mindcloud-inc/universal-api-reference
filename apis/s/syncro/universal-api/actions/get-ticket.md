# Syncro: Get Ticket

Retrieves a ticket from Syncro by ID.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-ticket?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-ticket?${params}`, {
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
| `id` | number | yes | The Syncro ticket ID. |

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

Through the native Syncro API, this operation is `GET /tickets/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

