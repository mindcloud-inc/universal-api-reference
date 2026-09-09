# Walmart: Get WFS Inventory



```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory?${params}`, {
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
| `sku` | string | no | Accepts multiple values as an array. |
| `shipNodeType` | list<string> | no | Filter results by ship-node type. - Only supported value is `multichannel`. - Use this parameter only if you are a multi-channel seller. - When you send `shipNodeType`, you must also send `sku`. All other query parameters are ignored. - `sku` can be a single value or several SKUs separated by commas (for example, "sku1,sku2"). Example: `multichannel`. |
| `gtin` | string | no |  |
| `fromModifiedDate` | string | no | The start of the last modified date range. Returns only inventory records updated on or after this timestamp. Use 24-hour UTC format `YYYY-MM-DD HH:mm:ss` (for example, `2025-06-01 00:00:00`). |
| `toModifiedDate` | string | no | The end of the last-modified date range. Returns only inventory records updated on or before this timestamp. Use the same `YYYY-MM-DD HH:mm:ss` format as `fromModifiedDate`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventory": [
        {
          "inventoryData": {
            "availableUnits": 1,
            "firstInStockDate": {},
            "inboundUnits": 1,
            "inventoryAge": {
              "0To90days": 1,
              "181To270days": 1,
              "271To365days": 1,
              "365PlusDays": 1,
              "91To180days": 1
            },
            "itemLifecycle": "string",
            "onhandUnits": 1,
            "publishingStatus": "string",
            "reservedUnits": 1,
            "stockStatus": "string",
            "unavailableUnits": {
              "inventoryMovementUnits": 1,
              "inventoryReviewUnits": 1
            }
          },
          "inventoryInsights": {
            "daysOfSupply": "string",
            "outOfStockDate": {},
            "salesForecastWeek1to4": {},
            "salesForecastWeek5to8": {},
            "salesForecastWeek9to12": {},
            "sellThroughRate": 1,
            "suggestedUnits": 1,
            "surplusUnits": {}
          },
          "itemInformation": {
            "brand": "string",
            "gtin": "string",
            "itemCondition": "string",
            "itemID": "string",
            "itemName": "Ava Chen",
            "offerID": "string",
            "sku": "string"
          }
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
| `inventory[].inventoryData.availableUnits` | number |  |
| `inventory[].inventoryData.firstInStockDate` | object |  |
| `inventory[].inventoryData.inboundUnits` | number |  |
| `inventory[].inventoryData.inventoryAge.0To90days` | number |  |
| `inventory[].inventoryData.inventoryAge.181To270days` | number |  |
| `inventory[].inventoryData.inventoryAge.271To365days` | number |  |
| `inventory[].inventoryData.inventoryAge.365PlusDays` | number |  |
| `inventory[].inventoryData.inventoryAge.91To180days` | number |  |
| `inventory[].inventoryData.itemLifecycle` | string |  |
| `inventory[].inventoryData.onhandUnits` | number |  |
| `inventory[].inventoryData.publishingStatus` | string |  |
| `inventory[].inventoryData.reservedUnits` | number |  |
| `inventory[].inventoryData.stockStatus` | string |  |
| `inventory[].inventoryData.unavailableUnits.inventoryMovementUnits` | number |  |
| `inventory[].inventoryData.unavailableUnits.inventoryReviewUnits` | number |  |
| `inventory[].inventoryInsights.daysOfSupply` | string |  |
| `inventory[].inventoryInsights.outOfStockDate` | object |  |
| `inventory[].inventoryInsights.salesForecastWeek1to4` | object |  |
| `inventory[].inventoryInsights.salesForecastWeek5to8` | object |  |
| `inventory[].inventoryInsights.salesForecastWeek9to12` | object |  |
| `inventory[].inventoryInsights.sellThroughRate` | number |  |
| `inventory[].inventoryInsights.suggestedUnits` | number |  |
| `inventory[].inventoryInsights.surplusUnits` | object |  |
| `inventory[].itemInformation.brand` | string |  |
| `inventory[].itemInformation.gtin` | string |  |
| `inventory[].itemInformation.itemCondition` | string |  |
| `inventory[].itemInformation.itemID` | string |  |
| `inventory[].itemInformation.itemName` | string |  |
| `inventory[].itemInformation.offerID` | string |  |
| `inventory[].itemInformation.sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/wfs/inventory` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wfs-inventory.md) for the provider-specific parameters and requirements.

