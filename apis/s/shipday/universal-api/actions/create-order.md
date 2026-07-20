# Shipday: Create Order

Creates a new delivery order in Shipday.

```
POST https://connect.mindcloud.co/v1/universal/shipday/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNumber": "99qT5A",
  "customerName": "Mr. Jhon Mason",
  "customerAddress": "556 Crestlake Dr, San Francisco, CA 94132, USA",
  "customerPhoneNumber": "+14152392212",
  "restaurantName": "Popeyes Louisiana Kitchen",
  "restaurantAddress": "890 Geneva Ave, San Francisco, CA 94112, United States"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNumber": "99qT5A",
    "customerName": "Mr. Jhon Mason",
    "customerAddress": "556 Crestlake Dr, San Francisco, CA 94132, USA",
    "customerPhoneNumber": "+14152392212",
    "restaurantName": "Popeyes Louisiana Kitchen",
    "restaurantAddress": "890 Geneva Ave, San Francisco, CA 94112, United States"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNumber` | string | yes | Alphanumeric identifier for the order. Example: `99qT5A`. |
| `customerName` | string | yes | Customer name for the order. Example: `Mr. Jhon Mason`. |
| `customerAddress` | string | yes | Customer delivery address. Example: `556 Crestlake Dr, San Francisco, CA 94132, USA`. |
| `customerEmail` | string | no | Customer email address. Example: `jhonMason@gmail.com`. |
| `customerPhoneNumber` | string | yes | Customer phone number with country code. Example: `+14152392212`. |
| `restaurantName` | string | yes | Restaurant name for the order. Example: `Popeyes Louisiana Kitchen`. |
| `restaurantAddress` | string | yes | Restaurant pickup address. Example: `890 Geneva Ave, San Francisco, CA 94112, United States`. |
| `restaurantPhoneNumber` | string | no | Restaurant phone number with country code. Example: `+14152392013`. |
| `expectedDeliveryDate` | date | no | Requested delivery date. Example: `2021-06-03`. |
| `expectedPickupTime` | date | no | Requested pickup time. Example: `17:45:00`. |
| `expectedDeliveryTime` | date | no | Requested delivery time. Example: `19:22:00`. |
| `orderItem[]` | array<object> | no | JSON array of order item objects. |
| `tips` | number | no | Tip amount for the order. Example: `2.5`. |
| `tax` | number | no | Tax amount for the order. Example: `1.5`. |
| `discountAmount` | number | no | Discount amount for the order. Example: `1.5`. |
| `deliveryFee` | number | no | Delivery fee charged for the order. Example: `3`. |
| `totalOrderCost` | number | no | Total order cost. Example: `13.47`. |
| `pickupInstruction` | string | no | Pickup instructions for the carrier. |
| `deliveryInstruction` | string | no | Delivery instructions for the carrier. Example: `fast`. |
| `paymentMethod` | string | no | Payment method for the order. Example: `credit_card`. |
| `pickup` | object | no | Pickup details object. |
| `dropoff` | object | no | Dropoff details object. |
| `orderSource` | string | no | Source of the order. Example: `Seamless`. |
| `additionalId` | string | no | Additional ID for the order. Example: `4532`. |
| `clientRestaurantId` | number | no | Client Restaurant ID. Example: `12`. |
| `creditCardType` | string | no | Type of the credit card when payment method is not cash. Example: `visa`. |
| `creditCardId` | number | no | Last four digits of the credit card when payment method is not cash. Example: `1234`. |
| `isCatering` | boolean | no | Marker of catering order. Example: `false`. |
| `pickup.address` | object | no | Address details. |
| `pickup.address.unit` | string | no | unit/address line 2 Example: `Suite 1`. |
| `pickup.address.street` | string | no | street/address line 1 Example: `890 Geneva Ave`. |
| `pickup.address.city` | string | no | Pickup address city. Example: `San Francisco`. |
| `pickup.address.state` | string | no | Pickup address state. Example: `CA`. |
| `pickup.address.zip` | string | no | Pickup address ZIP code. Example: `94112`. |
| `pickup.address.country` | string | no | Pickup address country code. Example: `US`. |
| `dropoff.address` | object | no | Address details. |
| `dropoff.address.unit` | string | no | unit/address line 2 Example: `Apt 2`. |
| `dropoff.address.street` | string | no | street/address line 1 Example: `556 Crestlake Dr`. |
| `dropoff.address.city` | string | no | Dropoff address city. Example: `San Francisco`. |
| `dropoff.address.state` | string | no | Dropoff address state. Example: `CA`. |
| `dropoff.address.zip` | string | no | Dropoff address ZIP code. Example: `94132`. |
| `dropoff.address.country` | string | no | Dropoff address country code. Example: `US`. |
| `orderItem[].name` | string | no | Name of the order item. Example: `Popcorn Shrimp`. |
| `orderItem[].quantity` | number | no | Quantity of the order item. Example: `3`. |
| `orderItem[].unitPrice` | number | no | Price of the order item per unit. Example: `2.99`. |
| `orderItem[].addOns[]` | array<string> | no | Array of add-on items. Example: `Sauce`. |
| `orderItem[].detail` | string | no | Detailed note for the order item. Example: `Please add less salt`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shipday API returns.

## Native endpoint

Through the native Shipday API, this operation is `POST /orders` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

