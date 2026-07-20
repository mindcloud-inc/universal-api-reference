# Create Order with Shipday

Creates a new delivery order in Shipday.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Create Order](https://docs.shipday.com/reference/insert-delivery-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | body | `string` | yes | Alphanumeric identifier for the order. |
| `customerName` | body | `string` | yes | Customer name for the order. |
| `customerAddress` | body | `string` | yes | Customer delivery address. |
| `customerEmail` | body | `string` | no | Customer email address. |
| `customerPhoneNumber` | body | `string` | yes | Customer phone number with country code. |
| `restaurantName` | body | `string` | yes | Restaurant name for the order. |
| `restaurantAddress` | body | `string` | yes | Restaurant pickup address. |
| `restaurantPhoneNumber` | body | `string` | no | Restaurant phone number with country code. |
| `expectedDeliveryDate` | body | `date` | no | Requested delivery date. |
| `expectedPickupTime` | body | `date` | no | Requested pickup time. |
| `expectedDeliveryTime` | body | `date` | no | Requested delivery time. |
| `orderItem[]` | body | `array<object>` | no | JSON array of order item objects. |
| `tips` | body | `number` | no | Tip amount for the order. |
| `tax` | body | `number` | no | Tax amount for the order. |
| `discountAmount` | body | `number` | no | Discount amount for the order. |
| `deliveryFee` | body | `number` | no | Delivery fee charged for the order. |
| `totalOrderCost` | body | `number` | no | Total order cost. |
| `pickupInstruction` | body | `string` | no | Pickup instructions for the carrier. |
| `deliveryInstruction` | body | `string` | no | Delivery instructions for the carrier. |
| `paymentMethod` | body | `string` | no | Payment method for the order. |
| `pickup` | body | `object` | no | Pickup details object. |
| `dropoff` | body | `object` | no | Dropoff details object. |
| `orderSource` | body | `string` | no | Source of the order. |
| `additionalId` | body | `string` | no | Additional ID for the order. |
| `clientRestaurantId` | body | `number` | no | Client Restaurant ID. |
| `creditCardType` | body | `string` | no | Type of the credit card when payment method is not cash. |
| `creditCardId` | body | `number` | no | Last four digits of the credit card when payment method is not cash. |
| `isCatering` | body | `boolean` | no | Marker of catering order. |
| `pickup.address` | body | `object` | no | Address details. |
| `pickup.address.unit` | body | `string` | no | unit/address line 2 |
| `pickup.address.street` | body | `string` | no | street/address line 1 |
| `pickup.address.city` | body | `string` | no | Pickup address city. |
| `pickup.address.state` | body | `string` | no | Pickup address state. |
| `pickup.address.zip` | body | `string` | no | Pickup address ZIP code. |
| `pickup.address.country` | body | `string` | no | Pickup address country code. |
| `dropoff.address` | body | `object` | no | Address details. |
| `dropoff.address.unit` | body | `string` | no | unit/address line 2 |
| `dropoff.address.street` | body | `string` | no | street/address line 1 |
| `dropoff.address.city` | body | `string` | no | Dropoff address city. |
| `dropoff.address.state` | body | `string` | no | Dropoff address state. |
| `dropoff.address.zip` | body | `string` | no | Dropoff address ZIP code. |
| `dropoff.address.country` | body | `string` | no | Dropoff address country code. |
| `orderItem[].name` | body | `string` | no | Name of the order item. |
| `orderItem[].quantity` | body | `number` | no | Quantity of the order item. |
| `orderItem[].unitPrice` | body | `number` | no | Price of the order item per unit. |
| `orderItem[].addOns[]` | body | `array<string>` | no | Array of add-on items. |
| `orderItem[].detail` | body | `string` | no | Detailed note for the order item. |
