# Amark: Create Order



```
POST https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNumber": "string",
  "shipMethod": "FEDEX",
  "shipperServiceCode": "EXPSVR",
  "billingLocation": {},
  "shippingLocation": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNumber": "string",
    "shipMethod": "FEDEX",
    "shipperServiceCode": "EXPSVR",
    "billingLocation": {},
    "shippingLocation": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNumber` | string | yes |  |
| `shipMethod` | list<string> | yes | One of: `FEDEX`, `UPS`, `USPS`, `VAULT`. |
| `shipperServiceCode` | list<string> | yes | One of: `EXPSVR`, `FIRST`, `FX2D`, `INTECO`, `PRIORITY`, `TRANSFER`. |
| `billingLocation` | object | yes |  |
| `shippingLocation` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | no |  |
| `orderDate` | date | no |  |
| `isDeliveryConfirm` | boolean | no |  |
| `isSignatureConfirm` | boolean | no |  |
| `isSignatureOverride` | boolean | no |  |
| `isForcedOverride` | boolean | no |  |
| `isInsured` | boolean | no |  |
| `isRegistered` | boolean | no |  |
| `items[]` | array<object> | no |  |
| `invoiceURL` | string | no |  |
| `totalUS` | number | no |  |
| `totalShipping` | number | no |  |
| `totalTax` | number | no |  |
| `totalAdjustment` | number | no |  |
| `orderNote` | string | no |  |
| `pickPackInstruction` | string | no |  |
| `invoiceData` | string | no |  |
| `gS1Data` | string | no |  |
| `paymentMethod` | string | no |  |
| `vaultAccount` | string | no |  |
| `custodian` | string | no |  |
| `isReship` | boolean | no |  |
| `feeAmount` | number | no |  |
| `isGift` | boolean | no |  |
| `giftMessage` | string | no |  |
| `feeLabel` | string | no |  |
| `isCostco` | number | no |  |
| `labelData` | string | no |  |
| `poNumber` | string | no |  |
| `canFulfill` | boolean | no |  |
| `paidStatus` | string | no |  |
| `items[].id` | number | no |  |
| `items[].sku` | string | no |  |
| `items[].description` | string | no |  |
| `items[].quantity` | number | no |  |
| `items[].totalUS` | number | no |  |
| `items[].harmonizedCode` | string | no |  |
| `items[].exportCode` | string | no |  |
| `items[].shipmentDetailDesc` | string | no |  |
| `items[].countryManufacture` | string | no |  |
| `items[].countryManufacture_Name` | string | no |  |
| `items[].poLineSequenceNumber` | number | no |  |
| `items[].costcoSKU` | string | no |  |
| `billingLocation.companyName` | string | no |  |
| `billingLocation.firstName` | string | no |  |
| `billingLocation.lastName` | string | no |  |
| `billingLocation.address1` | string | no |  |
| `billingLocation.address2` | string | no |  |
| `billingLocation.city` | string | no |  |
| `billingLocation.state` | string | no |  |
| `billingLocation.postalCode` | string | no |  |
| `billingLocation.countryISO` | string | no |  |
| `billingLocation.phone` | string | no |  |
| `billingLocation.email` | string | no |  |
| `billingLocation.is_residential` | boolean | no |  |
| `shippingLocation.companyName` | string | no |  |
| `shippingLocation.firstName` | string | no |  |
| `shippingLocation.lastName` | string | no |  |
| `shippingLocation.address1` | string | no |  |
| `shippingLocation.address2` | string | no |  |
| `shippingLocation.city` | string | no |  |
| `shippingLocation.state` | string | no |  |
| `shippingLocation.postalCode` | string | no |  |
| `shippingLocation.countryISO` | string | no |  |
| `shippingLocation.phone` | string | no |  |
| `shippingLocation.email` | string | no |  |
| `shippingLocation.is_residential` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amark API returns.

## Native endpoint

Through the native Amark API, this operation is `POST /Order/Create` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

