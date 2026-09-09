# Walmart: Get WFS Inventory (Legacy)



```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory-legacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory-legacy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-wfs-inventory-legacy?${params}`, {
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
| `sku` | string | no |  |
| `fromModifiedDate` | string | no |  |
| `toModifiedDate` | string | no |  |
| `shipNodeType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryData": {
        "availableUnits": 1,
        "firstInStockDate": "string",
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
        "outOfStockDate": "string",
        "salesForecastWeek1to4": 1,
        "salesForecastWeek5to8": 1,
        "salesForecastWeek9to12": {},
        "sellThroughRate": 1,
        "suggestedUnits": 1,
        "surplusUnits": 1
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryData.availableUnits` | number |  |
| `inventoryData.firstInStockDate` | string |  |
| `inventoryData.inboundUnits` | number |  |
| `inventoryData.inventoryAge.0To90days` | number |  |
| `inventoryData.inventoryAge.181To270days` | number |  |
| `inventoryData.inventoryAge.271To365days` | number |  |
| `inventoryData.inventoryAge.365PlusDays` | number |  |
| `inventoryData.inventoryAge.91To180days` | number |  |
| `inventoryData.itemLifecycle` | string |  |
| `inventoryData.onhandUnits` | number |  |
| `inventoryData.publishingStatus` | string |  |
| `inventoryData.reservedUnits` | number |  |
| `inventoryData.stockStatus` | string |  |
| `inventoryData.unavailableUnits.inventoryMovementUnits` | number |  |
| `inventoryData.unavailableUnits.inventoryReviewUnits` | number |  |
| `inventoryInsights.daysOfSupply` | string |  |
| `inventoryInsights.outOfStockDate` | string |  |
| `inventoryInsights.salesForecastWeek1to4` | number |  |
| `inventoryInsights.salesForecastWeek5to8` | number |  |
| `inventoryInsights.salesForecastWeek9to12` | object |  |
| `inventoryInsights.sellThroughRate` | number |  |
| `inventoryInsights.suggestedUnits` | number |  |
| `inventoryInsights.surplusUnits` | number |  |
| `itemInformation.brand` | string |  |
| `itemInformation.gtin` | string |  |
| `itemInformation.itemCondition` | string |  |
| `itemInformation.itemID` | string |  |
| `itemInformation.itemName` | string |  |
| `itemInformation.offerID` | string |  |
| `itemInformation.sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/fulfillment/inventory` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wfs-inventory-legacy.md) for the provider-specific parameters and requirements.

