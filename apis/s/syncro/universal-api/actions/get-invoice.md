# Syncro: Get Invoice

Retrieves an invoice from Syncro by ID or number.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-invoice?${params}`, {
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
| `id` | number | yes | Invoice identifier. Syncro's path schema documents this as an integer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceDue": "string",
      "contactId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customer": {
        "address": "string",
        "businessAndFullName": "Ava Chen",
        "businessName": "Ava Chen",
        "businessThenName": "Ava Chen",
        "city": "string",
        "contacts": [
          [
            {}
          ]
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "disabled": true,
        "email": "ava@example.com",
        "firstname": "Ava",
        "fullname": "Ava Chen",
        "getSms": true,
        "id": 1,
        "lastname": "Chen",
        "mobile": "string",
        "noEmail": true,
        "onlineProfileUrl": "https://example.com",
        "optOut": true,
        "phone": "string",
        "state": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "date": "2026-05-07T12:00:00.000Z",
      "dateReceived": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "hardwarecost": "string",
      "id": 1,
      "isPaid": true,
      "lineItems": [
        [
          {}
        ]
      ],
      "locationId": 1,
      "note": "string",
      "number": "string",
      "payments": [
        [
          {}
        ]
      ],
      "pdfUrl": "https://example.com",
      "poNumber": "string",
      "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
      "subtotal": "string",
      "tax": "string",
      "techMarkedPaid": true,
      "ticketId": 1,
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "verifiedPaid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceDue` | string |  |
| `contactId` | number |  |
| `createdAt` | date |  |
| `customer.address` | string |  |
| `customer.businessAndFullName` | string |  |
| `customer.businessName` | string |  |
| `customer.businessThenName` | string |  |
| `customer.city` | string |  |
| `customer.contacts[]` | array<object> |  |
| `customer.createdAt` | date |  |
| `customer.disabled` | boolean |  |
| `customer.email` | string |  |
| `customer.firstname` | string |  |
| `customer.fullname` | string |  |
| `customer.getSms` | boolean |  |
| `customer.id` | number |  |
| `customer.lastname` | string |  |
| `customer.mobile` | string |  |
| `customer.noEmail` | boolean |  |
| `customer.onlineProfileUrl` | string |  |
| `customer.optOut` | boolean |  |
| `customer.phone` | string |  |
| `customer.state` | string |  |
| `customer.updatedAt` | date |  |
| `date` | date |  |
| `dateReceived` | date |  |
| `dueDate` | date |  |
| `hardwarecost` | string |  |
| `id` | number |  |
| `isPaid` | boolean |  |
| `lineItems[]` | array<object> |  |
| `locationId` | number |  |
| `note` | string |  |
| `number` | string |  |
| `payments[]` | array<object> |  |
| `pdfUrl` | string |  |
| `poNumber` | string |  |
| `sinceUpdatedAt` | date |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `techMarkedPaid` | boolean |  |
| `ticketId` | number |  |
| `total` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `verifiedPaid` | boolean |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /invoices/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

