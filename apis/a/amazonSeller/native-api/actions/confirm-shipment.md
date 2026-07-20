# Confirm Shipment with Amazon Seller

Updates shipment confirmation for an Amazon Seller order.

## Endpoint

- **Method:** `POST`
- **Path:** `orders/v0/orders/:orderId/shipmentConfirmation`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Confirm Shipment](https://developer-docs.amazon.com/sp-api/reference/confirmshipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | An Amazon-defined order identifier, in 3-7-7 format. |
| `marketplaceId` | body | `list<string>` | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `orderItems[].orderItemId` | body | `string` | no | *required* The order item's unique identifier. |
| `orderItems[].quantity` | body | `string` | no | The items quantity. |
| `packageReferenceId` | body | `string` | yes | A seller-supplied identifier that uniquely identifies a package within the scope of an order. Only positive numeric values are supported. |
| `orderItems[].transparencyCodes` | body | `string` | no | A list of order items. (array of strings) Send multiple values as a array. |
| `shipDate` | body | `string` | yes | The shipping date for the package. Must be in ISO 8601 date/time format. |
| `carrierCode` | body | `string` | yes | Identifies the carrier that will deliver the package. This field is required for all marketplaces.  For more information, refer to the (Carrier Code announcement)[https://developer-docs.amazon.com/sp-api/changelog/carriercode-value-required-in-shipment-confirmations-for-br-mx-ca-sg-au-in-jp-marketplaces] |
| `carrierName` | body | `string` | no | Carrier name that will deliver the package. Required when carrierCode is "Other" |
| `trackingNumber` | body | `string` | yes | The tracking number used to obtain tracking and delivery information. |
| `orderItems[]` | body | `array<object>` | no | A list of order items. |
| `shippingMethod` | body | `string` | no | Ship method to be used for shipping the order. |
| `shipFromSupplySourceId` | body | `string` | no | The unique identifier for the supply source. |
| `codCollectionMethod` | body | `list<string>` | no | The COD collection method (only supported in the JP marketplace).  Allowed: `DirectPayment` |
