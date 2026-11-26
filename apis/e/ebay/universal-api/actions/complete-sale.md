# eBay: Complete Sale

Use this call to do various tasks after the creation of a single line item or multiple line item order.

```
PUT https://connect.mindcloud.co/v1/universal/ebay/latest/actions/complete-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/complete-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/complete-sale', {
  method: 'PUT',
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
| `feedbackInfo.targetUser` | string | no | This eBay User ID identifies the recipient user for whom the feedback is being left. This field is required in CompleteSale if the FeedbackInfo container is used. |
| `itemID` | string | no | Unique identifier for an eBay listing. An ItemID value can be paired up with a corresponding TransactionID value in a CompleteSale request to identify a single order line item. Alternatively, the OrderLineItemID value for the order line item can be used. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[]` | array<object> | no | Contains information about one order line item in a package. The package can contain multiple units of a given order line item, and multiple order line items. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[].countryOfOrigin` | string | no | The Country of Manufacture for the order line item; this is required for customs. This should identify the country in which more than 50% of the value of the item was created. This value must conform to the ISO 3166 two-letter country code standard. To see the list of currently supported codes, and the English names associated with each code (e.g., KY="Cayman Islands"), call GeteBayDetails with DetailName set to CountryDetails. |
| `shipment.shipmentTrackingDetails[].shippingCarrierUsed` | string | no | The name of the shipping carrier used to ship the item. This field and the ShipmentTrackingNumber field are mutually dependent. When you submit ShippingCarrierUsed, you must also supply a value for ShipmentTrackingNumber. When you submit ShipmentTrackingNumber, you must also supply a value for ShippingCarrierUsed. When the site ID is Austria, Poland, or UK, ShippingCarrierUsed can be any value, because it is not checked by eBay. For all other sites, only the following characters are allowed: letters (a-z, A-Z), numbers (0-9), space, and dash (-). The site ID is specified in the CompleteSale request header. *Note*: Commonly used shipping carriers can be found by calling GeteBayDetails with DetailName set to ShippingCarrierDetails and examining the returned ShippingCarrierDetails.ShippingCarrier field. ShippingCarrierCodeType also has a list of valid shipping carriers, but eBay cannot guarantee that this enumerated type contains a full, updated list of shipping carriers. *For the CompleteSale call:* - This field is not case sensitive in the CompleteSale request. - When using UPS Mail Innovations, supply the value UPS-MI. Buyers will subsequently be sent to the UPS Mail Innovations website for tracking status. - When using FedEx SmartPost, supply the value FedEx. Buyers will subsequently be sent to the FedEx web site for tracking status. |
| `shipment.shippedTime` | string | no | ( optional ) The date and time that the seller handed off the package(s) to the shipping carrier. If this field is not included in the request, the timestamp of the call execution is used as the shipped time. Note that sellers have the ability to set this value up to 3 calendar days in the future. |
| `feedbackInfo.commentText` | string | no | Textual comment that explains, clarifies, or justifies the Feedback rating specified in CommentType. This field is required in CompleteSale if the FeedbackInfo container is used. |
| `orderID` | string | no | A unique identifier for an eBay order. This field can be used to make an 'order-level' update. If an order has multiple line items, and the CompleteSale call is being used to update the status of, or provide feedback for a single line item within the order, the OrderLineItemID field or ItemID/TransactionID pair must be used to identify this order line item instead of the OrderID field. If the order only has one line item, it the OrderID field can be used to make any updates with the CompleteSale call. OrderID overrides an OrderLineItemID or ItemID/TransactionID pair if these fields are also specified in the same request. |
| `shipment.shipmentTrackingDetails[]` | array | no | Container consisting of the tracking number and shipping carrier associated with the shipment of one item (package). Because an order can have multiple line items and/or packages, there can be multiple ShipmentTrackingDetails containers under the Shipment container. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[].description` | string | no | The item description of the order line item, based on its ItemID. |
| `shipment.shipmentTrackingDetails[].shipmentTrackingNumber` | string | no | The tracking number assigned by the shipping carrier to the item shipment. This field and the ShippingCarrierUsed field are mutually dependent. When you submit ShipmentTrackingNumber, you must also supply a value for ShippingCarrierUsed. When you submit ShippingCarrierUsed, you must also supply a value for ShipmentTrackingNumber. The seller is responsible for the accuracy of the shipment tracking number, as eBay only verifies that the tracking number is consistent with the numbering scheme used by the specified shipping carrier, but cannot verify the accuracy of the tracking number. For order management calls, For GetOrders, GetSellerTransactions, and GetItemTransactions only: This field is only returned if a valid tracking number is set. With the exception of the GetSellerTransactions (where it is only returned to the seller and not buyer), the tracking number will only be returned to the seller or buyer. If a user is using a Trading WSDL Version 1019 or above, this field will only be returned to the buyer or seller, and no longer returned at all to third parties. If using a Trading WSDL older than Version 1019, this field is returned to third parties, but the string value returned in the field will be Unavailable. Note: The Trading API only supports alphanumeric characters for shipment tracking numbers, and any other characters are not supported, including spaces, hyphens, and all other special characters. Users should not enter spaces even if spaces are shown for the tracking number on the shipping label. |
| `orderLineItemID` | string | no | A unique identifier for an eBay order line item. OrderLineItemID values are returned (at the order line item level) in Trading API's order management calls. This identifier is created once there is a commitment to buy (bidder wins the auction, buyer clicks buy button, or buyer purchases item through PlaceOffer call). An OrderLineItemID value can be used in a CompleteSale request to identify a line item within an order. Alternatively, an ItemID/TransactionID pair can also be used to identify a line item. Unless an ItemID/TransactionID pair is used to identify an order line item, or an OrderID value is used to identify an order, the OrderLineItemID must be specified. If OrderLineItemID is specified, the ItemID/TransactionID pair are ignored if present in the same request. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem` | object | no | Contains information about one or more order line items in a Global Shipping Program package. Required or returned if the value of ShippingCarrierUsed is `PBI`. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[].itemID` | string | no | Unique identifier for the eBay listing associated with the order line item. A multiple-quantity listing can have multiple order line items, but only one ItemID value. Unless an OrderLineItemID or SKU value is specified in the same node, this field is required for each ItemTransactionID node included in the request. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[].transactionID` | string | no | Unique identifier for an eBay order line item (transaction). The TransactionID should match the ItemID specified in each ItemTransactionID node included in the request. Optionally, an OrderLineItemID value can substitute for the ItemID/TransactionID pair. The TransactionID value for auction listings is always 0 since there can be only one winning bidder/one sale for an auction listing. Note: Beginning in July 2024, non-zero transaction IDs will start being returned for auction listings. If necessary, update code to handle non-zero transaction IDs for auction transactions before this time. |
| `transactionID` | string | no | Unique identifier for a sales transaction. A TransactionID identifier is created once there is a commitment to buy (bidder wins the auction, buyer clicks buy button, or buyer purchases item through PlaceOffer call). The TransactionID can be paired up with the corresponding ItemID value in a CompleteSale request to identify a single order line item. Alternatively, the OrderLineItemID value for the order line item can be used. Unless an OrderLineItemID value is used to identify a single order line item, or the OrderID value is used to identify a single or multiple line item order, the ItemID/TransactionID pair must be specified. To perform an action on an entire multiple line item order, the OrderID field must be used. If an OrderID or OrderLineItemID value is specified, an ItemID/TransactionID pair will be ignored (if present in the same request). The TransactionID value for auction listings is always 0 since there can be only one winning bidder/one sale for an auction listing. Note: Beginning in July 2024, non-zero transaction IDs will start being returned for auction listings. If necessary, update code to handle non-zero transaction IDs for auction transactions before this time. |
| `paid` | boolean | no | Set this field to *'True'* to mark an unpaid order as paid. If the call is successful, the order line item(s) are marked as 'Paid' in eBay's system. *Note*: seller is not allowed to set this field to `False`. |
| `shipment.shipmentTrackingDetails[].shipmentLineItem.lineItem[].quantity` | number | no | The number of units of the order line item in this package; this is required for customs. The seller must ensure that this matches the quantity of the order line item enclosed in the package. This value must be a positive integer, and it can't be greater than the quantity of this item specified in the original transaction. This field is a required field in CompleteSale if the order type is a Global Shipping Program (GSP) order. |
| `shipped` | boolean | no | The seller includes and sets this field to true if the order or order line item has been shipped. If the call is successful, the order line item(s) are marked as Shipped in My eBay. If the seller includes and sets this field to false, the order or order line item are marked (or remain) as 'Not Shipped' in eBay's system. If this field is not included, the shipped status of the order or order line item remain unchanged in My eBay. If shipment tracking information is provided for an order or order line item through the Shipment container in the same request, the Shipped status is set to true automatically, and the Shipped field is not necessary. |
| `feedbackInfo` | object | no |  |
| `shipment` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `POST` (base URL `https://api.ebay.com/ws/api.dll`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-sale.md) for the provider-specific parameters and requirements.

