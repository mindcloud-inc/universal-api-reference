# Farmbrite: List orders

Retrieves a list of orders from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-orders?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
      "data": [
        {
          "cartId": "string",
          "chargeSubtotal": 1,
          "chargeTotal": 1,
          "contactId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "deliveryAmount": 1,
          "deliveryType": "string",
          "discountAmount": 1,
          "discountReason": "string",
          "dueDate": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "invoiceNumber": "string",
          "isAdmin": true,
          "isQuickpay": true,
          "lastName": "Chen",
          "memo": "string",
          "message": "string",
          "note": "string",
          "orderDate": "2026-05-07T12:00:00.000Z",
          "orderTotal": 1,
          "paymentDate": "string",
          "paymentMethod": "string",
          "paymentStatus": "string",
          "phone": "string",
          "pickedUpBy": "string",
          "pickList": "string",
          "pickupLocationId": "string",
          "poNumber": "string",
          "preparedBy": "string",
          "source": "string",
          "status": "string",
          "stripeId": "string",
          "taxesAmount": 1,
          "taxRate": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].cartId` | string |  |
| `data[].chargeSubtotal` | number |  |
| `data[].chargeTotal` | number |  |
| `data[].contactId` | string |  |
| `data[].createdAt` | date |  |
| `data[].createdBy` | string |  |
| `data[].deliveryAmount` | number |  |
| `data[].deliveryType` | string |  |
| `data[].discountAmount` | number |  |
| `data[].discountReason` | string |  |
| `data[].dueDate` | string |  |
| `data[].email` | string |  |
| `data[].firstName` | string |  |
| `data[].id` | string |  |
| `data[].invoiceNumber` | string |  |
| `data[].isAdmin` | boolean |  |
| `data[].isQuickpay` | boolean |  |
| `data[].lastName` | string |  |
| `data[].memo` | string |  |
| `data[].message` | string |  |
| `data[].note` | string |  |
| `data[].orderDate` | date |  |
| `data[].orderTotal` | number |  |
| `data[].paymentDate` | string |  |
| `data[].paymentMethod` | string |  |
| `data[].paymentStatus` | string |  |
| `data[].phone` | string |  |
| `data[].pickedUpBy` | string |  |
| `data[].pickList` | string |  |
| `data[].pickupLocationId` | string |  |
| `data[].poNumber` | string |  |
| `data[].preparedBy` | string |  |
| `data[].source` | string |  |
| `data[].status` | string |  |
| `data[].stripeId` | string |  |
| `data[].taxesAmount` | number |  |
| `data[].taxRate` | string |  |
| `data[].updatedAt` | date |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /orders` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

