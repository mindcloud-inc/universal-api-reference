# Farmbrite: Retrieve order

Retrieves a specific order from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-order?${params}`, {
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
| `orderId` | string | yes |  |

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

Through the native Farmbrite API, this operation is `GET /orders/:order_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

