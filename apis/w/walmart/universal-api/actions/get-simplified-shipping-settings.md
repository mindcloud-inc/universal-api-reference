# Walmart: Get Simplified Shipping Settings

Fetch the Simplified Shipping Settings for a seller account and FC level configurations.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-simplified-shipping-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-simplified-shipping-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-simplified-shipping-settings?${params}`, {
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
      "accountConfigs": {
        "carrierConfigs": [
          {
            "carriers": [
              {
                "carrierName": "Ava Chen",
                "carrierService": "string"
              }
            ],
            "configurations": [
              {
                "addressTypes": [
                  "string"
                ],
                "regions": [
                  {
                    "regionCode": "string",
                    "regionName": "Ava Chen"
                  }
                ],
                "shippingCharge": {
                  "perShippingCharge": {
                    "chargePerItem": {
                      "amount": 1,
                      "currency": "string"
                    },
                    "shippingAndHandling": {
                      "amount": 1,
                      "currency": "string"
                    },
                    "unitOfMeasure": "string"
                  },
                  "rateModelType": "string"
                }
              }
            ]
          }
        ],
        "migrateFreeShippingOffers": true,
        "shippingPriority": "string"
      },
      "shipNodeConfigs": [
        {
          "carrierConfigs": [
            {
              "carriers": [
                {
                  "carrierName": "Ava Chen",
                  "carrierService": "string"
                }
              ],
              "configurations": [
                {
                  "addressTypes": [
                    "string"
                  ],
                  "regions": [
                    {
                      "regionCode": "string",
                      "regionName": "Ava Chen"
                    }
                  ],
                  "shippingCharge": {
                    "perShippingCharge": {
                      "chargePerWeight": {
                        "amount": 1,
                        "currency": "string"
                      },
                      "shippingAndHandling": {
                        "amount": 1,
                        "currency": "string"
                      },
                      "unitOfMeasure": "string"
                    },
                    "rateModelType": "string"
                  }
                }
              ]
            }
          ],
          "isOverridden": true,
          "shipNodes": [
            "string"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountConfigs.carrierConfigs[].carriers[].carrierName` | string |  |
| `accountConfigs.carrierConfigs[].carriers[].carrierService` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].addressTypes[]` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].regions[].regionCode` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].regions[].regionName` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.perShippingCharge.chargePerItem.amount` | number |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.perShippingCharge.chargePerItem.currency` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.perShippingCharge.shippingAndHandling.amount` | number |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.perShippingCharge.shippingAndHandling.currency` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.perShippingCharge.unitOfMeasure` | string |  |
| `accountConfigs.carrierConfigs[].configurations[].shippingCharge.rateModelType` | string |  |
| `accountConfigs.migrateFreeShippingOffers` | boolean |  |
| `accountConfigs.shippingPriority` | string |  |
| `shipNodeConfigs[].carrierConfigs[].carriers[].carrierName` | string |  |
| `shipNodeConfigs[].carrierConfigs[].carriers[].carrierService` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].addressTypes[]` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].regions[].regionCode` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].regions[].regionName` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.perShippingCharge.chargePerWeight.amount` | number |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.perShippingCharge.chargePerWeight.currency` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.perShippingCharge.shippingAndHandling.amount` | number |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.perShippingCharge.shippingAndHandling.currency` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.perShippingCharge.unitOfMeasure` | string |  |
| `shipNodeConfigs[].carrierConfigs[].configurations[].shippingCharge.rateModelType` | string |  |
| `shipNodeConfigs[].isOverridden` | boolean |  |
| `shipNodeConfigs[].shipNodes[]` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/simplifiedshippingsettings` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-simplified-shipping-settings.md) for the provider-specific parameters and requirements.

