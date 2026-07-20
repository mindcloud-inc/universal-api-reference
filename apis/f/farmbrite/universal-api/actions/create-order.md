# Farmbrite: Create order

Creates a new order in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `email` | string | yes |  |

## Response

```json
{
  "success": true,
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `chargeSubtotal` | number |  |
| `chargeTotal` | number |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `deliveryAmount` | number |  |
| `deliveryType` | string |  |
| `discountAmount` | number |  |
| `discountReason` | string |  |
| `dueDate` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `invoiceNumber` | string |  |
| `isAdmin` | boolean |  |
| `isQuickpay` | boolean |  |
| `lastName` | string |  |
| `memo` | string |  |
| `message` | string |  |
| `note` | string |  |
| `orderDate` | date |  |
| `orderTotal` | number |  |
| `paymentDate` | string |  |
| `paymentMethod` | string |  |
| `paymentStatus` | string |  |
| `phone` | string |  |
| `pickedUpBy` | string |  |
| `pickList` | string |  |
| `pickupLocationId` | string |  |
| `poNumber` | string |  |
| `preparedBy` | string |  |
| `source` | string |  |
| `status` | string |  |
| `stripeId` | string |  |
| `taxesAmount` | number |  |
| `taxRate` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Farmbrite API, this operation is `POST /orders` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

