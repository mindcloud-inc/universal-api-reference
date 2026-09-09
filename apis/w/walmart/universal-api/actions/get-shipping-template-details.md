# Walmart: Get Shipping Template Details

Get Shipping Template Details of CUSTOM, DEFAULT & 3PL-specific templates.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-details?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-details?${params}`, {
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
| `templateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": 1,
      "fcDetails": {
        "countryName": "Ava Chen",
        "fulfillmentCenterIds": [
          "string"
        ],
        "isoCountryCode": "string"
      },
      "id": "string",
      "modifiedDate": 1,
      "name": "Ava Chen",
      "rateModelType": "string",
      "shippingMethods": [
        {
          "configurations": [
            {
              "addressTypes": [
                "string"
              ],
              "regions": [
                {
                  "regionCode": "string",
                  "regionName": "Ava Chen",
                  "subRegions": [
                    {
                      "states": [
                        {
                          "stateCode": "string",
                          "stateName": "Ava Chen",
                          "stateSubregions": [
                            {
                              "stateSubregionCode": "string",
                              "stateSubregionName": "Ava Chen"
                            }
                          ]
                        }
                      ],
                      "subRegionCode": "string",
                      "subRegionName": "Ava Chen"
                    }
                  ]
                }
              ],
              "tieredShippingCharges": [
                {
                  "maxLimit": 1,
                  "minLimit": 1,
                  "shipCharge": {
                    "amount": 1,
                    "currency": "string"
                  }
                }
              ],
              "transitTime": 1
            }
          ],
          "shipMethod": "string",
          "status": "string"
        }
      ],
      "shippingType": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | number |  |
| `fcDetails.countryName` | string |  |
| `fcDetails.fulfillmentCenterIds[]` | string |  |
| `fcDetails.isoCountryCode` | string |  |
| `id` | string |  |
| `modifiedDate` | number |  |
| `name` | string |  |
| `rateModelType` | string |  |
| `shippingMethods[].configurations[].addressTypes[]` | string |  |
| `shippingMethods[].configurations[].regions[].regionCode` | string |  |
| `shippingMethods[].configurations[].regions[].regionName` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].states[].stateCode` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].states[].stateName` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].states[].stateSubregions[].stateSubregionCode` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].states[].stateSubregions[].stateSubregionName` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].subRegionCode` | string |  |
| `shippingMethods[].configurations[].regions[].subRegions[].subRegionName` | string |  |
| `shippingMethods[].configurations[].tieredShippingCharges[].maxLimit` | number |  |
| `shippingMethods[].configurations[].tieredShippingCharges[].minLimit` | number |  |
| `shippingMethods[].configurations[].tieredShippingCharges[].shipCharge.amount` | number |  |
| `shippingMethods[].configurations[].tieredShippingCharges[].shipCharge.currency` | string |  |
| `shippingMethods[].configurations[].transitTime` | number |  |
| `shippingMethods[].shipMethod` | string |  |
| `shippingMethods[].status` | string |  |
| `shippingType` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/templates/:templateId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-template-details.md) for the provider-specific parameters and requirements.

