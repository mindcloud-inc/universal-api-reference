# TikTok Shop: Get Order Detail



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-detail?${params}`, {
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
| `ids` | string<string> | no | A list of TikTok Shop order ID values. **max: 50 per request** Accepts multiple values as an array. |
| `shopCipher` | list<list> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationRequired": true,
      "buyerAvatar": "string",
      "buyerEmail": "ava@example.com",
      "buyerMessage": "string",
      "buyerNickname": "Ava Chen",
      "cancelOrderSlaTime": 1,
      "createTime": 1,
      "deliveryOptionId": "string",
      "deliveryOptionName": "Ava Chen",
      "deliverySlaTime": 1,
      "deliveryType": "string",
      "fulfillmentType": "string",
      "hasUpdatedRecipientAddress": true,
      "id": "string",
      "isCod": true,
      "isExchangeOrder": true,
      "isOnHoldOrder": true,
      "isRefundableSample": true,
      "isReplacementOrder": true,
      "isSampleOrder": true,
      "isSubscriptionOrder": true,
      "lineItems": [
        {
          "currency": "string",
          "displayStatus": "string",
          "id": "string",
          "isDangerousGood": true,
          "isGift": true,
          "isPodCustomized": true,
          "itemTax": [
            {
              "taxAmount": "string",
              "taxRate": "string",
              "taxType": "string"
            }
          ],
          "originalPrice": "string",
          "platformDiscount": "string",
          "productId": "string",
          "productName": "Ava Chen",
          "salePrice": "string",
          "sellerDiscount": "string",
          "sellerSku": "string",
          "skuId": "string",
          "skuImage": "string",
          "skuName": "Ava Chen",
          "skuType": "string",
          "trackingNumber": "string"
        }
      ],
      "packages": [
        "string"
      ],
      "paidTime": 1,
      "payment": {
        "currency": "string",
        "itemInsuranceTax": "string",
        "originalShippingFee": "string",
        "originalTotalProductPrice": "string",
        "platformDiscount": "string",
        "productTax": "string",
        "sellerDiscount": "string",
        "shippingFee": "string",
        "shippingFeeCofundedDiscount": "string",
        "shippingFeePlatformDiscount": "string",
        "shippingFeeSellerDiscount": "string",
        "shippingFeeTax": "string",
        "subTotal": "string",
        "tax": "string",
        "totalAmount": "string"
      },
      "paymentMethodName": "Ava Chen",
      "recipientAddress": {
        "addressDetail": "string",
        "addressLine1": "string",
        "addressLine2": "string",
        "addressLine3": "string",
        "addressLine4": "string",
        "districtInfo": [
          {
            "addressLevel": "string",
            "addressLevelName": "Ava Chen",
            "addressName": "Ava Chen",
            "isoCode": "string"
          }
        ],
        "firstName": "Ava",
        "fullAddress": "string",
        "lastName": "Chen",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "postalCode": "string",
        "regionCode": "string"
      },
      "rtsSlaTime": 1,
      "shippingDueTime": 1,
      "shippingType": "string",
      "status": "string",
      "ttsSlaTime": 1,
      "updateTime": 1,
      "userId": "string",
      "warehouseId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationRequired` | boolean |  |
| `buyerAvatar` | string |  |
| `buyerEmail` | string |  |
| `buyerMessage` | string |  |
| `buyerNickname` | string |  |
| `cancelOrderSlaTime` | number |  |
| `createTime` | number |  |
| `deliveryOptionId` | string |  |
| `deliveryOptionName` | string |  |
| `deliverySlaTime` | number |  |
| `deliveryType` | string |  |
| `fulfillmentType` | string |  |
| `hasUpdatedRecipientAddress` | boolean |  |
| `id` | string |  |
| `isCod` | boolean |  |
| `isExchangeOrder` | boolean |  |
| `isOnHoldOrder` | boolean |  |
| `isRefundableSample` | boolean |  |
| `isReplacementOrder` | boolean |  |
| `isSampleOrder` | boolean |  |
| `isSubscriptionOrder` | boolean |  |
| `lineItems` | array<object> |  |
| `lineItems[].currency` | string |  |
| `lineItems[].displayStatus` | string |  |
| `lineItems[].id` | string |  |
| `lineItems[].isDangerousGood` | boolean |  |
| `lineItems[].isGift` | boolean |  |
| `lineItems[].isPodCustomized` | boolean |  |
| `lineItems[].itemTax` | array<object> |  |
| `lineItems[].itemTax[].taxAmount` | string |  |
| `lineItems[].itemTax[].taxRate` | string |  |
| `lineItems[].itemTax[].taxType` | string |  |
| `lineItems[].originalPrice` | string |  |
| `lineItems[].platformDiscount` | string |  |
| `lineItems[].productId` | string |  |
| `lineItems[].productName` | string |  |
| `lineItems[].salePrice` | string |  |
| `lineItems[].sellerDiscount` | string |  |
| `lineItems[].sellerSku` | string |  |
| `lineItems[].skuId` | string |  |
| `lineItems[].skuImage` | string |  |
| `lineItems[].skuName` | string |  |
| `lineItems[].skuType` | string |  |
| `lineItems[].trackingNumber` | string |  |
| `packages` | array |  |
| `paidTime` | number |  |
| `payment` | object |  |
| `payment.currency` | string |  |
| `payment.itemInsuranceTax` | string |  |
| `payment.originalShippingFee` | string |  |
| `payment.originalTotalProductPrice` | string |  |
| `payment.platformDiscount` | string |  |
| `payment.productTax` | string |  |
| `payment.sellerDiscount` | string |  |
| `payment.shippingFee` | string |  |
| `payment.shippingFeeCofundedDiscount` | string |  |
| `payment.shippingFeePlatformDiscount` | string |  |
| `payment.shippingFeeSellerDiscount` | string |  |
| `payment.shippingFeeTax` | string |  |
| `payment.subTotal` | string |  |
| `payment.tax` | string |  |
| `payment.totalAmount` | string |  |
| `paymentMethodName` | string |  |
| `recipientAddress` | object |  |
| `recipientAddress.addressDetail` | string |  |
| `recipientAddress.addressLine1` | string |  |
| `recipientAddress.addressLine2` | string |  |
| `recipientAddress.addressLine3` | string |  |
| `recipientAddress.addressLine4` | string |  |
| `recipientAddress.districtInfo` | array<object> |  |
| `recipientAddress.districtInfo[].addressLevel` | string |  |
| `recipientAddress.districtInfo[].addressLevelName` | string |  |
| `recipientAddress.districtInfo[].addressName` | string |  |
| `recipientAddress.districtInfo[].isoCode` | string |  |
| `recipientAddress.firstName` | string |  |
| `recipientAddress.fullAddress` | string |  |
| `recipientAddress.lastName` | string |  |
| `recipientAddress.name` | string |  |
| `recipientAddress.phoneNumber` | string |  |
| `recipientAddress.postalCode` | string |  |
| `recipientAddress.regionCode` | string |  |
| `rtsSlaTime` | number |  |
| `shippingDueTime` | number |  |
| `shippingType` | string |  |
| `status` | string |  |
| `ttsSlaTime` | number |  |
| `updateTime` | number |  |
| `userId` | string |  |
| `warehouseId` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET order/202309/orders` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-detail.md) for the provider-specific parameters and requirements.

