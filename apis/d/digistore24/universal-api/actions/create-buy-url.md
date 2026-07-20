# Digistore24: Create Buy URL

Creates a customized buy URL in Digistore24.

```
POST https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-buy-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-buy-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-buy-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product ID |
| `buyer` | object | no | Buyer object |
| `buyer.email` | string | no |  |
| `buyer.salutation` | string | no |  |
| `buyer.title` | string | no |  |
| `buyer.lastName` | string | no |  |
| `buyer.firstName` | string | no |  |
| `buyer.company` | string | no |  |
| `buyer.street` | string | no |  |
| `buyer.city` | string | no |  |
| `buyer.zipcode` | string | no |  |
| `buyer.state` | string | no |  |
| `buyer.country` | string | no |  |
| `buyer.phoneNo` | string | no |  |
| `buyer.taxId` | string | no |  |
| `buyer.readonlyKeys` | string | no |  |
| `buyer.id` | string | no |  |
| `paymentPlan` | object | no | Payment plan object |
| `paymentPlan.firstAmount` | number | no |  |
| `paymentPlan.otherAmounts` | number | no |  |
| `paymentPlan.currency` | string | no |  |
| `paymentPlan.numberOfInstallments` | number | no |  |
| `paymentPlan.firstBillingInterval` | string | no |  |
| `paymentPlan.otherBillingIntervals` | string | no |  |
| `paymentPlan.testInterval` | string | no |  |
| `paymentPlan.template` | string | no |  |
| `paymentPlan.upgradeOrderId` | string | no |  |
| `paymentPlan.upgradeType` | string | no |  |
| `paymentPlan.taxMode` | string | no |  |
| `tracking` | object | no | Tracking object |
| `tracking.custom` | string | no |  |
| `tracking.affiliate` | string | no |  |
| `tracking.affiliatePriority` | string | no |  |
| `tracking.campaignkey` | string | no |  |
| `tracking.trackingkey` | string | no |  |
| `tracking.utmSource` | string | no |  |
| `tracking.utmMedium` | string | no |  |
| `tracking.utmCampaign` | string | no |  |
| `tracking.utmTerm` | string | no |  |
| `tracking.utmContent` | string | no |  |
| `validUntil` | string | no | Validity end date/time |
| `urls` | object | no | Redirect URLs object |
| `urls.thankyouUrl` | string | no |  |
| `urls.fallbackUrl` | string | no |  |
| `urls.upgradeErrorUrl` | string | no |  |
| `placeholders` | object | no | Placeholder replacements object |
| `settings` | object | no | Buy URL settings object |
| `settings.orderformId` | string | no |  |
| `settings.affiliateCommissionRate` | number | no |  |
| `settings.affiliateCommissionFix` | number | no |  |
| `settings.voucherCode` | string | no |  |
| `settings.voucher1stRate` | number | no |  |
| `settings.voucherOthRates` | number | no |  |
| `settings.voucher1stAmount` | number | no |  |
| `settings.voucherOthAmounts` | number | no |  |
| `settings.forceRebilling` | boolean | no |  |
| `settings.payMethods[]` | array<string> | no |  |
| `addons[]` | array<object> | no | Addon list |
| `addons[].productId` | string | no |  |
| `addons[].firstAmount` | number | no |  |
| `addons[].otherAmounts` | number | no |  |
| `addons[].singleAmount` | number | no |  |
| `addons[].defaultQuantity` | number | no |  |
| `addons[].maxQuantityType` | string | no |  |
| `addons[].maxQuantity` | number | no |  |
| `addons[].currency` | string | no | Three-character currency code for the add-on. |
| `addons[].isQuantityEditableBeforePurchase` | string | no | Whether the buyer can change the add-on quantity before purchase. |
| `addons[].isQuantityEditableAfterPurchase` | string | no | Whether the buyer can change the add-on quantity after purchase. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `POST /createBuyUrl` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-buy-url.md) for the provider-specific parameters and requirements.

