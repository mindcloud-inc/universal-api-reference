# Coast: Get Policy By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicy?connectionId=$CONNECTION_ID&policyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicy?${params}`, {
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
| `policyId` | string | yes | Coast policy ID of the policy to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "actionOnFuelUpExceedingTankSpace": {
        "mode": "string"
      },
      "allowedPurchaseTimeWindows": {},
      "archived": true,
      "createdTime": "string",
      "dailySignOut": {},
      "enableMobileFleetCardUsage": true,
      "enablePolicyExceptions": true,
      "exclusivelyAllowedMerchantBrands": {
        "hasMoreItems": true
      },
      "exclusivelyAllowedMerchantLocations": {
        "hasMoreItems": true
      },
      "fuelFinderRestriction": {},
      "gpsControls": {},
      "id": "string",
      "missingFuelFromTank": {},
      "name": "Ava Chen",
      "requireOdometerBeforeFuel": true,
      "requireVehicleForVehicleRelatedPurchases": true,
      "signOutAfterPurchase": {},
      "spendControls": {
        "fleetAndMaintenance": {
          "allowedMerchantCategories": {
            "categories": [
              {
                "id": 1,
                "key": "string",
                "name": "Ava Chen"
              }
            ],
            "type": "string"
          },
          "individualPurchaseAmountLimit": {},
          "memoThresholdAmount": {},
          "numberOfPurchases": {},
          "receiptThresholdAmount": {},
          "totalSpend": {
            "amount": 1,
            "timeFrame": "string"
          }
        },
        "fuel": {
          "allowedMerchantCategories": {
            "categories": [
              {
                "id": 1,
                "key": "string",
                "name": "Ava Chen"
              }
            ],
            "type": "string"
          },
          "individualPurchaseAmountLimit": {},
          "memoThresholdAmount": {},
          "numberOfPurchases": {},
          "receiptThresholdAmount": {},
          "totalSpend": {
            "amount": 1,
            "timeFrame": "string"
          }
        },
        "generalBusiness": {
          "allowedMerchantCategories": {
            "categories": [
              {
                "id": 1,
                "key": "string",
                "name": "Ava Chen"
              }
            ],
            "type": "string"
          },
          "individualPurchaseAmountLimit": {},
          "memoThresholdAmount": {},
          "numberOfPurchases": {},
          "receiptThresholdAmount": {},
          "totalSpend": {}
        },
        "global": {},
        "materialsAndSupplies": {
          "allowedMerchantCategories": {
            "categories": [
              {
                "id": 1,
                "key": "string",
                "name": "Ava Chen"
              }
            ],
            "type": "string"
          },
          "individualPurchaseAmountLimit": {},
          "memoThresholdAmount": {},
          "numberOfPurchases": {},
          "receiptThresholdAmount": {},
          "totalSpend": {}
        },
        "travelAndRestaurants": {
          "allowedMerchantCategories": {
            "categories": [
              {
                "id": 1,
                "key": "string",
                "name": "Ava Chen"
              }
            ],
            "type": "string"
          },
          "individualPurchaseAmountLimit": {},
          "memoThresholdAmount": {},
          "numberOfPurchases": {},
          "receiptThresholdAmount": {},
          "totalSpend": {}
        }
      },
      "timezone": "string",
      "type": "string",
      "unnecessaryRefuel": {},
      "updatedTime": "string",
      "wrongFuelType": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `actionOnFuelUpExceedingTankSpace.mode` | string |  |
| `allowedPurchaseTimeWindows` | object |  |
| `archived` | boolean |  |
| `createdTime` | string |  |
| `dailySignOut` | object |  |
| `enableMobileFleetCardUsage` | boolean |  |
| `enablePolicyExceptions` | boolean |  |
| `exclusivelyAllowedMerchantBrands.hasMoreItems` | boolean |  |
| `exclusivelyAllowedMerchantLocations.hasMoreItems` | boolean |  |
| `fuelFinderRestriction` | object |  |
| `gpsControls` | object |  |
| `id` | string |  |
| `missingFuelFromTank` | object |  |
| `name` | string |  |
| `requireOdometerBeforeFuel` | boolean |  |
| `requireVehicleForVehicleRelatedPurchases` | boolean |  |
| `signOutAfterPurchase` | object |  |
| `spendControls.fleetAndMaintenance.allowedMerchantCategories.categories[].id` | number |  |
| `spendControls.fleetAndMaintenance.allowedMerchantCategories.categories[].key` | string |  |
| `spendControls.fleetAndMaintenance.allowedMerchantCategories.categories[].name` | string |  |
| `spendControls.fleetAndMaintenance.allowedMerchantCategories.type` | string |  |
| `spendControls.fleetAndMaintenance.individualPurchaseAmountLimit` | object |  |
| `spendControls.fleetAndMaintenance.memoThresholdAmount` | object |  |
| `spendControls.fleetAndMaintenance.numberOfPurchases` | object |  |
| `spendControls.fleetAndMaintenance.receiptThresholdAmount` | object |  |
| `spendControls.fleetAndMaintenance.totalSpend.amount` | number |  |
| `spendControls.fleetAndMaintenance.totalSpend.timeFrame` | string |  |
| `spendControls.fuel.allowedMerchantCategories.categories[].id` | number |  |
| `spendControls.fuel.allowedMerchantCategories.categories[].key` | string |  |
| `spendControls.fuel.allowedMerchantCategories.categories[].name` | string |  |
| `spendControls.fuel.allowedMerchantCategories.type` | string |  |
| `spendControls.fuel.individualPurchaseAmountLimit` | object |  |
| `spendControls.fuel.memoThresholdAmount` | object |  |
| `spendControls.fuel.numberOfPurchases` | object |  |
| `spendControls.fuel.receiptThresholdAmount` | object |  |
| `spendControls.fuel.totalSpend.amount` | number |  |
| `spendControls.fuel.totalSpend.timeFrame` | string |  |
| `spendControls.generalBusiness.allowedMerchantCategories.categories[].id` | number |  |
| `spendControls.generalBusiness.allowedMerchantCategories.categories[].key` | string |  |
| `spendControls.generalBusiness.allowedMerchantCategories.categories[].name` | string |  |
| `spendControls.generalBusiness.allowedMerchantCategories.type` | string |  |
| `spendControls.generalBusiness.individualPurchaseAmountLimit` | object |  |
| `spendControls.generalBusiness.memoThresholdAmount` | object |  |
| `spendControls.generalBusiness.numberOfPurchases` | object |  |
| `spendControls.generalBusiness.receiptThresholdAmount` | object |  |
| `spendControls.generalBusiness.totalSpend` | object |  |
| `spendControls.global` | object |  |
| `spendControls.materialsAndSupplies.allowedMerchantCategories.categories[].id` | number |  |
| `spendControls.materialsAndSupplies.allowedMerchantCategories.categories[].key` | string |  |
| `spendControls.materialsAndSupplies.allowedMerchantCategories.categories[].name` | string |  |
| `spendControls.materialsAndSupplies.allowedMerchantCategories.type` | string |  |
| `spendControls.materialsAndSupplies.individualPurchaseAmountLimit` | object |  |
| `spendControls.materialsAndSupplies.memoThresholdAmount` | object |  |
| `spendControls.materialsAndSupplies.numberOfPurchases` | object |  |
| `spendControls.materialsAndSupplies.receiptThresholdAmount` | object |  |
| `spendControls.materialsAndSupplies.totalSpend` | object |  |
| `spendControls.travelAndRestaurants.allowedMerchantCategories.categories[].id` | number |  |
| `spendControls.travelAndRestaurants.allowedMerchantCategories.categories[].key` | string |  |
| `spendControls.travelAndRestaurants.allowedMerchantCategories.categories[].name` | string |  |
| `spendControls.travelAndRestaurants.allowedMerchantCategories.type` | string |  |
| `spendControls.travelAndRestaurants.individualPurchaseAmountLimit` | object |  |
| `spendControls.travelAndRestaurants.memoThresholdAmount` | object |  |
| `spendControls.travelAndRestaurants.numberOfPurchases` | object |  |
| `spendControls.travelAndRestaurants.receiptThresholdAmount` | object |  |
| `spendControls.travelAndRestaurants.totalSpend` | object |  |
| `timezone` | string |  |
| `type` | string |  |
| `unnecessaryRefuel` | object |  |
| `updatedTime` | string |  |
| `wrongFuelType` | object |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/policies/:policyId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getpolicy.md) for the provider-specific parameters and requirements.

