# BigCommerce: Get Orders

Gets all orders

```
GET https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-orders?${params}`, {
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
| `status_id` | string | no | Status Identifier of the orders you want |
| `min_date_modified` | string | no | Minimum date the order was modified in RFC-2822 or ISO-8601. RFC-2822: Thu, 20 Apr 2017 11:32:00 -0400 ISO-8601: 2017-04-20T11:32:00.000-04:00 |
| `maxDateModified` | string | no |  |
| `minDateCreated` | string | no | Minimum date the order was created in RFC-2822 or ISO-8601. RFC-2822: Thu, 20 Apr 2017 11:32:00 -0400 ISO-8601: 2017-04-20T11:32:00.000-04:00 |
| `maxDateCreated` | string | no |  |
| `minId` | string | no | The minimum order ID. |
| `maxID` | string | no |  |
| `externalOrderID` | string | no | The order ID in another system, such as the Amazon Order ID if this is an Amazon order. |
| `channelID` | string | no | The channel ID of the sales channel the shopper used to place the order. |
| `include` | string | no | Allowed: consignments \| consignments.line_items \| fees |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseHandlingCost": "string",
      "baseShippingCost": "string",
      "baseWrappingCost": "string",
      "billingAddress": {
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "phone": "string",
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zip": "string"
      },
      "cartId": {},
      "channelId": 1,
      "consignments": {
        "resource": "string",
        "url": "https://example.com"
      },
      "couponDiscount": "string",
      "coupons": {
        "resource": "string",
        "url": "https://example.com"
      },
      "creditCardType": "string",
      "currencyCode": "string",
      "currencyExchangeRate": "string",
      "currencyId": 1,
      "customerId": 1,
      "customerLocale": "string",
      "customerMessage": "string",
      "customStatus": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "dateShipped": "string",
      "defaultCurrencyCode": "string",
      "defaultCurrencyId": 1,
      "discountAmount": "string",
      "ebayOrderId": "string",
      "externalId": {},
      "externalMerchantId": {},
      "externalOrderId": "string",
      "externalSource": {},
      "fees": {
        "resource": "string",
        "url": "https://example.com"
      },
      "geoipCountry": "string",
      "geoipCountryIso2": "string",
      "giftCertificateAmount": "string",
      "handlingCostExTax": "string",
      "handlingCostIncTax": "string",
      "handlingCostTax": "string",
      "handlingCostTaxClassId": 1,
      "id": 1,
      "ipAddress": "string",
      "ipAddressV6": "string",
      "isDeleted": true,
      "isEmailOptIn": true,
      "isTaxInclusivePricing": true,
      "itemsShipped": 1,
      "itemsTotal": 1,
      "orderIsDigital": true,
      "orderSource": "string",
      "paymentMethod": "string",
      "paymentProviderId": "string",
      "paymentStatus": "string",
      "products": {
        "resource": "string",
        "url": "https://example.com"
      },
      "refundedAmount": "string",
      "shippingAddressCount": 1,
      "shippingAddresses": {
        "resource": "string",
        "url": "https://example.com"
      },
      "shippingCostExTax": "string",
      "shippingCostIncTax": "string",
      "shippingCostTax": "string",
      "shippingCostTaxClassId": 1,
      "staffNotes": "string",
      "status": "string",
      "statusId": 1,
      "storeCreditAmount": "string",
      "storeDefaultCurrencyCode": "string",
      "storeDefaultToTransactionalExchangeRate": "string",
      "subtotalExTax": "string",
      "subtotalIncTax": "string",
      "subtotalTax": "string",
      "taxProviderId": "string",
      "totalExTax": "string",
      "totalIncTax": "string",
      "totalTax": "string",
      "wrappingCostExTax": "string",
      "wrappingCostIncTax": "string",
      "wrappingCostTax": "string",
      "wrappingCostTaxClassId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseHandlingCost` | string |  |
| `baseShippingCost` | string |  |
| `baseWrappingCost` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.company` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.countryIso2` | string |  |
| `billingAddress.email` | string |  |
| `billingAddress.firstName` | string |  |
| `billingAddress.lastName` | string |  |
| `billingAddress.phone` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.street1` | string |  |
| `billingAddress.street2` | string |  |
| `billingAddress.zip` | string |  |
| `cartId` | object |  |
| `channelId` | number |  |
| `consignments.resource` | string |  |
| `consignments.url` | string |  |
| `couponDiscount` | string |  |
| `coupons.resource` | string |  |
| `coupons.url` | string |  |
| `creditCardType` | string |  |
| `currencyCode` | string |  |
| `currencyExchangeRate` | string |  |
| `currencyId` | number |  |
| `customerId` | number |  |
| `customerLocale` | string |  |
| `customerMessage` | string |  |
| `customStatus` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `dateShipped` | string |  |
| `defaultCurrencyCode` | string |  |
| `defaultCurrencyId` | number |  |
| `discountAmount` | string |  |
| `ebayOrderId` | string |  |
| `externalId` | object |  |
| `externalMerchantId` | object |  |
| `externalOrderId` | string |  |
| `externalSource` | object |  |
| `fees.resource` | string |  |
| `fees.url` | string |  |
| `geoipCountry` | string |  |
| `geoipCountryIso2` | string |  |
| `giftCertificateAmount` | string |  |
| `handlingCostExTax` | string |  |
| `handlingCostIncTax` | string |  |
| `handlingCostTax` | string |  |
| `handlingCostTaxClassId` | number |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `ipAddressV6` | string |  |
| `isDeleted` | boolean |  |
| `isEmailOptIn` | boolean |  |
| `isTaxInclusivePricing` | boolean |  |
| `itemsShipped` | number |  |
| `itemsTotal` | number |  |
| `orderIsDigital` | boolean |  |
| `orderSource` | string |  |
| `paymentMethod` | string |  |
| `paymentProviderId` | string |  |
| `paymentStatus` | string |  |
| `products.resource` | string |  |
| `products.url` | string |  |
| `refundedAmount` | string |  |
| `shippingAddressCount` | number |  |
| `shippingAddresses.resource` | string |  |
| `shippingAddresses.url` | string |  |
| `shippingCostExTax` | string |  |
| `shippingCostIncTax` | string |  |
| `shippingCostTax` | string |  |
| `shippingCostTaxClassId` | number |  |
| `staffNotes` | string |  |
| `status` | string |  |
| `statusId` | number |  |
| `storeCreditAmount` | string |  |
| `storeDefaultCurrencyCode` | string |  |
| `storeDefaultToTransactionalExchangeRate` | string |  |
| `subtotalExTax` | string |  |
| `subtotalIncTax` | string |  |
| `subtotalTax` | string |  |
| `taxProviderId` | string |  |
| `totalExTax` | string |  |
| `totalIncTax` | string |  |
| `totalTax` | string |  |
| `wrappingCostExTax` | string |  |
| `wrappingCostIncTax` | string |  |
| `wrappingCostTax` | string |  |
| `wrappingCostTaxClassId` | number |  |

## Native endpoint

Through the native BigCommerce API, this operation is `GET /v2/orders` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-orders.md) for the provider-specific parameters and requirements.

