# SalesDrive: Create Order

Creates a new order in SalesDrive.

```
POST https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/create-order', {
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
| `fName` | string | no | Customer first name. |
| `lName` | string | no | Customer last name. |
| `phone` | string | no | Customer phone number. |
| `email` | string | no | Customer email address. |
| `products[]` | array<object> | no | Array of products for the order. |
| `paymentMethod` | string | no | Payment method. |
| `shippingMethod` | string | no | Shipping method. |
| `shippingAddress` | string | no | Delivery address. |
| `comment` | string | no | Order comment. |
| `externalId` | string | no | External order number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": 1,
      "success": true,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | number |  |
| `success` | boolean |  |
| `userId` | number |  |

## Native endpoint

Through the native SalesDrive API, this operation is `POST /handler/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

