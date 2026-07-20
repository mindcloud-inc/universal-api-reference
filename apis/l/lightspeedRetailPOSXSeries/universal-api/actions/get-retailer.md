# Lightspeed Retail POS (X-Series): Get Retailer

Retrieves retailer information from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountStatus": "string",
      "accountType": "string",
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "createCustomerByEmailReceipt": "ava@example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "culture": "string",
      "currency": {},
      "defaultDimensionsUnit": "string",
      "defaultTaxId": "string",
      "defaultWeightUnit": "string",
      "disableOnboardingTour": true,
      "discountProductId": "string",
      "domainPrefix": "string",
      "ecwidOnboardingSurveyState": "string",
      "embeddedBarcodeOption": "string",
      "enabledIntegrations": [
        {}
      ],
      "enabledPlatformApps": [
        {}
      ],
      "enableLineItemConsolidation": true,
      "giftCards": {},
      "hasWebRegister": true,
      "id": "string",
      "labelPrinterFormat": "string",
      "lightspeedUniqueId": "string",
      "loyalty": {},
      "marketCode": "string",
      "marketSegment": "string",
      "name": "Ava Chen",
      "noTaxGroupId": "string",
      "onAccount": {},
      "registerMigrationDate": "2026-05-07T12:00:00.000Z",
      "requirePasswordOnUserSwitch": "string",
      "restrictionState": "string",
      "restrictionStateReason": "string",
      "signupIndustryVertical": "string",
      "skuSequence": {},
      "ssoEnabled": true,
      "storeCredit": true,
      "storeUrl": "https://example.com",
      "subscription": {},
      "subscriptionPlanVersion": 1,
      "taxExclusive": true,
      "termsAndConditions": {},
      "timezone": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountStatus` | string |  |
| `accountType` | string |  |
| `activatedAt` | date |  |
| `country` | string |  |
| `createCustomerByEmailReceipt` | string |  |
| `createdAt` | date |  |
| `culture` | string |  |
| `currency` | object |  |
| `defaultDimensionsUnit` | string |  |
| `defaultTaxId` | string |  |
| `defaultWeightUnit` | string |  |
| `disableOnboardingTour` | boolean |  |
| `discountProductId` | string |  |
| `domainPrefix` | string |  |
| `ecwidOnboardingSurveyState` | string |  |
| `embeddedBarcodeOption` | string |  |
| `enabledIntegrations` | array<object> |  |
| `enabledPlatformApps` | array<object> |  |
| `enableLineItemConsolidation` | boolean |  |
| `giftCards` | object |  |
| `hasWebRegister` | boolean |  |
| `id` | string |  |
| `labelPrinterFormat` | string |  |
| `lightspeedUniqueId` | string |  |
| `loyalty` | object |  |
| `marketCode` | string |  |
| `marketSegment` | string |  |
| `name` | string |  |
| `noTaxGroupId` | string |  |
| `onAccount` | object |  |
| `registerMigrationDate` | date |  |
| `requirePasswordOnUserSwitch` | string |  |
| `restrictionState` | string |  |
| `restrictionStateReason` | string |  |
| `signupIndustryVertical` | string |  |
| `skuSequence` | object |  |
| `ssoEnabled` | boolean |  |
| `storeCredit` | boolean |  |
| `storeUrl` | string |  |
| `subscription` | object |  |
| `subscriptionPlanVersion` | number |  |
| `taxExclusive` | boolean |  |
| `termsAndConditions` | object |  |
| `timezone` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2026-04/retailer` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-retailer.md) for the provider-specific parameters and requirements.

