# Rithum for Brands: Create Order



```
POST https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].sku": "string",
  "profileId": 1,
  "items[].unitPrice": 1,
  "siteName": "Ava Chen",
  "items[].quantity": 1,
  "totalPrice": 1,
  "totalShippingPrice": 1,
  "buyerEmailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].sku": "string",
    "profileId": 1,
    "items[].unitPrice": 1,
    "siteName": "Ava Chen",
    "items[].quantity": 1,
    "totalPrice": 1,
    "totalShippingPrice": 1,
    "buyerEmailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[].sku` | string | yes |  |
| `profileId` | list<number> | yes |  |
| `items[].unitPrice` | number | yes |  |
| `siteName` | list | yes |  |
| `items[].quantity` | number | yes |  |
| `siteOrderID` | string | no |  |
| `items[].taxPrice` | number | no |  |
| `totalPrice` | number | yes |  |
| `items[].shippingPrice` | number | no |  |
| `totalTaxPrice` | number | no |  |
| `items[].shippingTaxPrice` | number | no |  |
| `totalShippingPrice` | number | yes |  |
| `totalShippingTaxPrice` | number | no |  |
| `estimatedShipDateUtc` | date | no |  |
| `checkoutStatus` | list | no |  |
| `paymentStatus` | list | no |  |
| `shippingStatus` | list | no |  |
| `buyerUserId` | string | no |  |
| `buyerEmailAddress` | string | yes |  |
| `paymentMethod` | string | no |  |
| `paymentCreditCardLast4` | string | no |  |
| `paymentMerchantReferenceNumber` | string | no |  |
| `shippingTitle` | string | no |  |
| `shippingFirstName` | string | no |  |
| `shippingLastName` | string | no |  |
| `shippingSuffix` | string | no |  |
| `shippingCompanyName` | string | no |  |
| `shippingCompanyJobTitle` | string | no |  |
| `shippingDaytimePhone` | string | no |  |
| `shippingEveningPhone` | string | no |  |
| `createdDateUtc` | date | no |  |
| `shippingAddressLine1` | string | no |  |
| `shippingAddressLine2` | string | no |  |
| `shippingCity` | string | no |  |
| `shippingStateOrProvince` | string | no |  |
| `shippingPostalCode` | string | no |  |
| `shippingCountry` | string | no |  |
| `billingTitle` | string | no |  |
| `billingFirstName` | string | no |  |
| `billingLastName` | string | no |  |
| `billingSuffix` | string | no |  |
| `billingCompanyName` | string | no |  |
| `billingCompanyJobTitle` | string | no |  |
| `billingDaytimePhone` | string | no |  |
| `billingEveningPhone` | string | no |  |
| `billingAddressLine1` | string | no |  |
| `billingAddressLine2` | string | no |  |
| `billingCity` | string | no |  |
| `billingStateOrProvince` | string | no |  |
| `billingPostalCode` | string | no |  |
| `billingCountry` | string | no |  |
| `items[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string"
      },
      "additionalCostOrDiscount": 1,
      "billingAddressLine1": "string",
      "billingAddressLine2": "string",
      "billingCity": "string",
      "billingCompanyJobTitle": {},
      "billingCompanyName": {},
      "billingCountry": "string",
      "billingDaytimePhone": {},
      "billingEveningPhone": {},
      "billingFirstName": "Ava",
      "billingLastName": "Chen",
      "billingPostalCode": "string",
      "billingStateOrProvince": {},
      "billingStateOrProvinceName": {},
      "billingSuffix": "string",
      "billingTitle": {},
      "buyerEmailAddress": "ava@example.com",
      "buyerEmailOptIn": true,
      "buyerUserId": "string",
      "checkoutDateUtc": {},
      "checkoutSourceID": {},
      "checkoutStatus": "string",
      "createdDateUtc": "string",
      "currency": "string",
      "deliverByDateUtc": {},
      "distributionCenterTypeRollup": "string",
      "estimatedShipDateUtc": {},
      "flagDescription": {},
      "flagID": 1,
      "giftOptionsTaxType": "string",
      "id": 1,
      "importDateUtc": "string",
      "orderTags": "string",
      "orderTaxType": "string",
      "paymentCreditCardLast4": "string",
      "paymentDateUtc": {},
      "paymentMerchantReferenceNumber": {},
      "paymentMethod": "string",
      "paymentPaypalAccountID": {},
      "paymentStatus": "string",
      "paymentTransactionID": {},
      "privateNotes": "string",
      "profileID": 1,
      "promotionAmount": 1,
      "promotionCode": {},
      "publicNotes": {},
      "requestedShippingCarrier": {},
      "requestedShippingClass": {},
      "resellerID": {},
      "secondarySiteOrderID": {},
      "sellerOrderID": {},
      "shippingAddressLine1": {},
      "shippingAddressLine2": {},
      "shippingCity": {},
      "shippingCompanyJobTitle": {},
      "shippingCompanyName": {},
      "shippingCountry": "string",
      "shippingDateUtc": {},
      "shippingDaytimePhone": {},
      "shippingEveningPhone": {},
      "shippingFirstName": {},
      "shippingLastName": {},
      "shippingPostalCode": {},
      "shippingStateOrProvince": {},
      "shippingStateOrProvinceName": {},
      "shippingStatus": "string",
      "shippingSuffix": {},
      "shippingTaxType": "string",
      "shippingTitle": {},
      "siteAccountID": {},
      "siteID": 1,
      "siteName": "Ava Chen",
      "siteOrderID": "string",
      "specialInstructions": "string",
      "totalGiftOptionPrice": 1,
      "totalGiftOptionTaxPrice": 1,
      "totalInsurancePrice": 1,
      "totalPrice": 1,
      "totalShippingPrice": 1,
      "totalShippingTaxPrice": 1,
      "totalTaxPrice": 1,
      "updatedDateUtc": "string",
      "userDataPresent": 1,
      "userDataRemovalDateUTC": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `additionalCostOrDiscount` | number |  |
| `billingAddressLine1` | string |  |
| `billingAddressLine2` | string |  |
| `billingCity` | string |  |
| `billingCompanyJobTitle` | object |  |
| `billingCompanyName` | object |  |
| `billingCountry` | string |  |
| `billingDaytimePhone` | object |  |
| `billingEveningPhone` | object |  |
| `billingFirstName` | string |  |
| `billingLastName` | string |  |
| `billingPostalCode` | string |  |
| `billingStateOrProvince` | object |  |
| `billingStateOrProvinceName` | object |  |
| `billingSuffix` | string |  |
| `billingTitle` | object |  |
| `buyerEmailAddress` | string |  |
| `buyerEmailOptIn` | boolean |  |
| `buyerUserId` | string |  |
| `checkoutDateUtc` | object |  |
| `checkoutSourceID` | object |  |
| `checkoutStatus` | string |  |
| `createdDateUtc` | string |  |
| `currency` | string |  |
| `deliverByDateUtc` | object |  |
| `distributionCenterTypeRollup` | string |  |
| `estimatedShipDateUtc` | object |  |
| `flagDescription` | object |  |
| `flagID` | number |  |
| `giftOptionsTaxType` | string |  |
| `id` | number |  |
| `importDateUtc` | string |  |
| `orderTags` | string |  |
| `orderTaxType` | string |  |
| `paymentCreditCardLast4` | string |  |
| `paymentDateUtc` | object |  |
| `paymentMerchantReferenceNumber` | object |  |
| `paymentMethod` | string |  |
| `paymentPaypalAccountID` | object |  |
| `paymentStatus` | string |  |
| `paymentTransactionID` | object |  |
| `privateNotes` | string |  |
| `profileID` | number |  |
| `promotionAmount` | number |  |
| `promotionCode` | object |  |
| `publicNotes` | object |  |
| `requestedShippingCarrier` | object |  |
| `requestedShippingClass` | object |  |
| `resellerID` | object |  |
| `secondarySiteOrderID` | object |  |
| `sellerOrderID` | object |  |
| `shippingAddressLine1` | object |  |
| `shippingAddressLine2` | object |  |
| `shippingCity` | object |  |
| `shippingCompanyJobTitle` | object |  |
| `shippingCompanyName` | object |  |
| `shippingCountry` | string |  |
| `shippingDateUtc` | object |  |
| `shippingDaytimePhone` | object |  |
| `shippingEveningPhone` | object |  |
| `shippingFirstName` | object |  |
| `shippingLastName` | object |  |
| `shippingPostalCode` | object |  |
| `shippingStateOrProvince` | object |  |
| `shippingStateOrProvinceName` | object |  |
| `shippingStatus` | string |  |
| `shippingSuffix` | object |  |
| `shippingTaxType` | string |  |
| `shippingTitle` | object |  |
| `siteAccountID` | object |  |
| `siteID` | number |  |
| `siteName` | string |  |
| `siteOrderID` | string |  |
| `specialInstructions` | string |  |
| `totalGiftOptionPrice` | number |  |
| `totalGiftOptionTaxPrice` | number |  |
| `totalInsurancePrice` | number |  |
| `totalPrice` | number |  |
| `totalShippingPrice` | number |  |
| `totalShippingTaxPrice` | number |  |
| `totalTaxPrice` | number |  |
| `updatedDateUtc` | string |  |
| `userDataPresent` | number |  |
| `userDataRemovalDateUTC` | object |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Orders/Create` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

