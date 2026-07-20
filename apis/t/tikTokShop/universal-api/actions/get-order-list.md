# TikTok Shop: Get Order List



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-list?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-order-list?${params}`, {
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
| `buyerUserId` | string | no |  |
| `createTimeGe` | date | no |  |
| `createTimeLt` | date | no |  |
| `isBuyerRequestCancel` | boolean | no |  |
| `orderStatus` | list<string> | no |  |
| `shippingType` | list<string> | no |  |
| `shopCipher` | list<string> | yes |  |
| `sortField` | string | no |  |
| `sortOrder` | string | no |  |
| `updateTimeGe` | date | no |  |
| `updateTimeLt` | date | no |  |
| `warehouseIds` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyerEmail": "ava@example.com",
      "buyerMessage": "string",
      "cancelOrderSlaTime": "2026-05-07T12:00:00.000Z",
      "collectionTime": "2026-05-07T12:00:00.000Z",
      "createTime": "2026-05-07T12:00:00.000Z",
      "deliveryOptionId": "string",
      "deliveryOptionName": "Ava Chen",
      "deliverySlaTime": "2026-05-07T12:00:00.000Z",
      "deliveryTime": "2026-05-07T12:00:00.000Z",
      "deliveryType": "string",
      "fulfillmentType": "string",
      "hasUpdatedRecipientAddress": true,
      "id": "string",
      "isCod": true,
      "isExchangeOrder": true,
      "isOnHoldOrder": true,
      "isReplacementOrder": true,
      "isSampleOrder": true,
      "lineItems": [
        {
          "currency": "string",
          "displayStatus": "string",
          "id": "string",
          "isDangerousGood": true,
          "isGift": true,
          "itemTax": [
            {
              "taxAmount": "string",
              "taxRate": "string",
              "taxType": "string"
            }
          ],
          "originalPrice": "string",
          "packageId": "string",
          "packageStatus": "string",
          "platformDiscount": "string",
          "productId": "string",
          "productName": "Ava Chen",
          "rtsTime": "2026-05-07T12:00:00.000Z",
          "salePrice": "string",
          "sellerDiscount": "string",
          "sellerSku": "string",
          "shippingProviderId": "string",
          "shippingProviderName": "Ava Chen",
          "skuId": "string",
          "skuImage": "string",
          "skuName": "Ava Chen",
          "skuType": "string",
          "trackingNumber": "string"
        }
      ],
      "packages": [
        {
          "id": "string"
        }
      ],
      "paidTime": "2026-05-07T12:00:00.000Z",
      "payment": {
        "currency": "string",
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
            "addressName": "Ava Chen"
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
      "rtsSlaTime": "2026-05-07T12:00:00.000Z",
      "rtsTime": "2026-05-07T12:00:00.000Z",
      "shippingProvider": "string",
      "shippingProviderId": "string",
      "shippingType": "string",
      "status": "string",
      "trackingNumber": "string",
      "ttsSlaTime": "2026-05-07T12:00:00.000Z",
      "updateTime": "2026-05-07T12:00:00.000Z",
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
| `buyerEmail` | string |  |
| `buyerMessage` | string |  |
| `cancelOrderSlaTime` | date |  |
| `collectionTime` | date |  |
| `createTime` | date |  |
| `deliveryOptionId` | string |  |
| `deliveryOptionName` | string |  |
| `deliverySlaTime` | date |  |
| `deliveryTime` | date |  |
| `deliveryType` | string |  |
| `fulfillmentType` | string |  |
| `hasUpdatedRecipientAddress` | boolean |  |
| `id` | string |  |
| `isCod` | boolean |  |
| `isExchangeOrder` | boolean |  |
| `isOnHoldOrder` | boolean |  |
| `isReplacementOrder` | boolean |  |
| `isSampleOrder` | boolean |  |
| `lineItems[].currency` | string |  |
| `lineItems[].displayStatus` | string |  |
| `lineItems[].id` | string |  |
| `lineItems[].isDangerousGood` | boolean |  |
| `lineItems[].isGift` | boolean |  |
| `lineItems[].itemTax[].taxAmount` | string |  |
| `lineItems[].itemTax[].taxRate` | string |  |
| `lineItems[].itemTax[].taxType` | string |  |
| `lineItems[].originalPrice` | string |  |
| `lineItems[].packageId` | string |  |
| `lineItems[].packageStatus` | string |  |
| `lineItems[].platformDiscount` | string |  |
| `lineItems[].productId` | string |  |
| `lineItems[].productName` | string |  |
| `lineItems[].rtsTime` | date |  |
| `lineItems[].salePrice` | string |  |
| `lineItems[].sellerDiscount` | string |  |
| `lineItems[].sellerSku` | string |  |
| `lineItems[].shippingProviderId` | string |  |
| `lineItems[].shippingProviderName` | string |  |
| `lineItems[].skuId` | string |  |
| `lineItems[].skuImage` | string |  |
| `lineItems[].skuName` | string |  |
| `lineItems[].skuType` | string |  |
| `lineItems[].trackingNumber` | string |  |
| `packages[].id` | string |  |
| `paidTime` | date |  |
| `payment.currency` | string |  |
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
| `recipientAddress.addressDetail` | string |  |
| `recipientAddress.addressLine1` | string |  |
| `recipientAddress.addressLine2` | string |  |
| `recipientAddress.addressLine3` | string |  |
| `recipientAddress.addressLine4` | string |  |
| `recipientAddress.districtInfo[].addressLevel` | string |  |
| `recipientAddress.districtInfo[].addressLevelName` | string |  |
| `recipientAddress.districtInfo[].addressName` | string |  |
| `recipientAddress.firstName` | string |  |
| `recipientAddress.fullAddress` | string |  |
| `recipientAddress.lastName` | string |  |
| `recipientAddress.name` | string |  |
| `recipientAddress.phoneNumber` | string |  |
| `recipientAddress.postalCode` | string |  |
| `recipientAddress.regionCode` | string |  |
| `rtsSlaTime` | date |  |
| `rtsTime` | date |  |
| `shippingProvider` | string |  |
| `shippingProviderId` | string |  |
| `shippingType` | string |  |
| `status` | string |  |
| `trackingNumber` | string |  |
| `ttsSlaTime` | date |  |
| `updateTime` | date |  |
| `userId` | string |  |
| `warehouseId` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `POST order/202309/orders/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-order-list.md) for the provider-specific parameters and requirements.

