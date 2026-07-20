# RO App: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | Invoice ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "createdAt": 1,
      "dueDate": 1,
      "id": 1,
      "idLabel": "string",
      "issueDate": 1,
      "managerId": 1,
      "payer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "paymentType": 1,
      "products": [
        {
          "amount": 1,
          "id": 1,
          "price": 1,
          "title": "string"
        }
      ],
      "status": 1,
      "statusFull": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `client.email` | string |  |
| `client.id` | number |  |
| `client.name` | string |  |
| `createdAt` | number |  |
| `dueDate` | number |  |
| `id` | number |  |
| `idLabel` | string |  |
| `issueDate` | number |  |
| `managerId` | number |  |
| `payer` | object |  |
| `payer.id` | number |  |
| `payer.name` | string |  |
| `paymentType` | number |  |
| `products` | array<object> |  |
| `products[].amount` | number |  |
| `products[].id` | number |  |
| `products[].price` | number |  |
| `products[].title` | string |  |
| `status` | number |  |
| `statusFull` | object |  |
| `statusFull.color` | string |  |
| `statusFull.id` | number |  |
| `statusFull.name` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /invoices/:invoice_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

