# Coast: Get All Policies



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpolicies?${params}`, {
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
| `nextPageToken` | string | no | A token that represents the next page of results. This token is returned in the response of a previous request and should be used to retrieve the next set of results. If not provided, the first page of results will be returned. |
| `pageSize` | number | no | The maximum number of results to return per page. If this parameter is not specified, the page size will be 10. This parameter works in conjunction with pagination tokens. |
| `archived` | boolean | no | Return archived responses |
| `type` | list | no | Return archived responses One of: `0`, `1`. |

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
      "allowedPurchaseTimeWindows": {
        "friday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        },
        "monday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        },
        "saturday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        },
        "sunday": {
          "spendWindow": "string"
        },
        "thursday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        },
        "tuesday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        },
        "wednesday": {
          "end": "string",
          "spendWindow": "string",
          "start": "string"
        }
      },
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
          "totalSpend": {}
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
| `allowedPurchaseTimeWindows.friday.end` | string |  |
| `allowedPurchaseTimeWindows.friday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.friday.start` | string |  |
| `allowedPurchaseTimeWindows.monday.end` | string |  |
| `allowedPurchaseTimeWindows.monday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.monday.start` | string |  |
| `allowedPurchaseTimeWindows.saturday.end` | string |  |
| `allowedPurchaseTimeWindows.saturday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.saturday.start` | string |  |
| `allowedPurchaseTimeWindows.sunday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.thursday.end` | string |  |
| `allowedPurchaseTimeWindows.thursday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.thursday.start` | string |  |
| `allowedPurchaseTimeWindows.tuesday.end` | string |  |
| `allowedPurchaseTimeWindows.tuesday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.tuesday.start` | string |  |
| `allowedPurchaseTimeWindows.wednesday.end` | string |  |
| `allowedPurchaseTimeWindows.wednesday.spendWindow` | string |  |
| `allowedPurchaseTimeWindows.wednesday.start` | string |  |
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
| `spendControls.fleetAndMaintenance.totalSpend` | object |  |
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

Through the native Coast API, this operation is `GET /v2/policies` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/getpolicies.md) for the provider-specific parameters and requirements.

