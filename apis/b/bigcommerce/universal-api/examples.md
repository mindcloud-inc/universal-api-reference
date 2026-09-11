# BigCommerce Universal API Examples

These examples use the MindCloud API key and BigCommerce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Orders

Gets all orders

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

Example response:

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

See the full [Get Orders action reference](actions/get-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigcommerce/latest/actions/get-orders).

## Add Cart Item



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/add-cart-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cartId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/add-cart-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cartId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Cart Item action reference](actions/add-cart-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigcommerce/latest/actions/add-cart-item).
