# Phemex: List Products



```
GET https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phemex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-products?${params}`, {
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
      "currencies": [
        {
          "assetsPrecision": 1,
          "code": 1,
          "currency": "string",
          "displayCurrency": "string",
          "inAssetsDisplay": 1,
          "maxValueEv": 1,
          "minValueEv": 1,
          "name": "Ava Chen",
          "needAddrTag": 1,
          "perpetual": 1,
          "spotInnoStatus": 1,
          "stableCoin": 1,
          "status": "string",
          "timestamp": "string",
          "valueScale": 1
        }
      ],
      "leverageMargins": [
        {
          "index_id": 1,
          "items": [
            {
              "maintenanceAmountRv": "string",
              "maintenanceMarginRateRr": "string",
              "maxLeverage": 1,
              "notionalValueRv": 1
            }
          ]
        }
      ],
      "leverages": [
        {
          "initialMargin": "string",
          "initialMarginEr": 1,
          "options": [
            1
          ]
        }
      ],
      "leveragesV2": [
        {
          "initialMarginRr": "string",
          "options": [
            1
          ]
        }
      ],
      "md5Checksum": "string",
      "perpProductsPilot": "string",
      "perpProductsV2": [
        {
          "baseCurrency": "string",
          "code": 1,
          "contractUnderlyingAssets": "string",
          "defaultLeverage": "string",
          "description": "string",
          "displaySymbol": "string",
          "fundingInterval": 1,
          "fundingRate8hSymbol": "string",
          "fundingRateSymbol": "string",
          "indexSymbol": "string",
          "leverageMargin": 1,
          "listTime": 1,
          "majorSymbol": true,
          "markSymbol": "string",
          "maxLeverage": 1,
          "maxOI": 1,
          "maxOpenPosLeverage": 1,
          "maxOrderQtyRq": "string",
          "maxPriceRp": "string",
          "minOrderValueRv": "string",
          "minPriceRp": "string",
          "perpProductSubType": "string",
          "pricePrecision": 1,
          "priceScale": 1,
          "qtyPrecision": 1,
          "qtyStepSize": "string",
          "quoteCurrency": "string",
          "ratioScale": 1,
          "settleCurrency": "string",
          "status": "string",
          "symbol": "string",
          "tickSize": "string",
          "tipOrderQty": 1,
          "tipOrderQtyRq": "string",
          "type": "string"
        }
      ],
      "products": [
        {
          "code": 1,
          "contractSize": 1,
          "contractUnderlyingAssets": "string",
          "defaultLeverage": "string",
          "description": "string",
          "displaySymbol": "string",
          "fundingInterval": 1,
          "fundingRate8hSymbol": "string",
          "fundingRateSymbol": "string",
          "indexSymbol": "string",
          "leverageMargin": 1,
          "listTime": 1,
          "lotSize": 1,
          "majorSymbol": true,
          "markSymbol": "string",
          "maxLeverage": 1,
          "maxOI": 1,
          "maxOrderQty": 1,
          "maxPriceEp": 1,
          "minPriceEp": 1,
          "pricePrecision": 1,
          "priceScale": 1,
          "quoteCurrency": "string",
          "ratioScale": 1,
          "settleCurrency": "string",
          "status": "string",
          "symbol": "string",
          "tickSize": 1,
          "tipOrderQty": 1,
          "type": "string"
        }
      ],
      "ratioScale": 1,
      "riskLimits": [
        {
          "riskLimits": [
            {
              "initialMargin": "string",
              "initialMarginEr": 1,
              "limit": 1,
              "maintenanceMargin": "string",
              "maintenanceMarginEr": 1
            }
          ],
          "steps": "string",
          "symbol": "string"
        }
      ],
      "riskLimitsV2": [
        {
          "riskLimits": [
            {
              "initialMarginRr": "string",
              "limit": 1,
              "maintenanceMarginRr": "string"
            }
          ],
          "steps": "string",
          "symbol": "string"
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
| `currencies[].assetsPrecision` | number |  |
| `currencies[].code` | number |  |
| `currencies[].currency` | string |  |
| `currencies[].displayCurrency` | string |  |
| `currencies[].inAssetsDisplay` | number |  |
| `currencies[].maxValueEv` | number |  |
| `currencies[].minValueEv` | number |  |
| `currencies[].name` | string |  |
| `currencies[].needAddrTag` | number |  |
| `currencies[].perpetual` | number |  |
| `currencies[].spotInnoStatus` | number |  |
| `currencies[].stableCoin` | number |  |
| `currencies[].status` | string |  |
| `currencies[].timestamp` | string |  |
| `currencies[].valueScale` | number |  |
| `leverageMargins[].index_id` | number |  |
| `leverageMargins[].items[].maintenanceAmountRv` | string |  |
| `leverageMargins[].items[].maintenanceMarginRateRr` | string |  |
| `leverageMargins[].items[].maxLeverage` | number |  |
| `leverageMargins[].items[].notionalValueRv` | number |  |
| `leverages[].initialMargin` | string |  |
| `leverages[].initialMarginEr` | number |  |
| `leverages[].options[]` | number |  |
| `leveragesV2[].initialMarginRr` | string |  |
| `leveragesV2[].options[]` | number |  |
| `md5Checksum` | string |  |
| `perpProductsPilot` | string |  |
| `perpProductsV2[].baseCurrency` | string |  |
| `perpProductsV2[].code` | number |  |
| `perpProductsV2[].contractUnderlyingAssets` | string |  |
| `perpProductsV2[].defaultLeverage` | string |  |
| `perpProductsV2[].description` | string |  |
| `perpProductsV2[].displaySymbol` | string |  |
| `perpProductsV2[].fundingInterval` | number |  |
| `perpProductsV2[].fundingRate8hSymbol` | string |  |
| `perpProductsV2[].fundingRateSymbol` | string |  |
| `perpProductsV2[].indexSymbol` | string |  |
| `perpProductsV2[].leverageMargin` | number |  |
| `perpProductsV2[].listTime` | number |  |
| `perpProductsV2[].majorSymbol` | boolean |  |
| `perpProductsV2[].markSymbol` | string |  |
| `perpProductsV2[].maxLeverage` | number |  |
| `perpProductsV2[].maxOI` | number |  |
| `perpProductsV2[].maxOpenPosLeverage` | number |  |
| `perpProductsV2[].maxOrderQtyRq` | string |  |
| `perpProductsV2[].maxPriceRp` | string |  |
| `perpProductsV2[].minOrderValueRv` | string |  |
| `perpProductsV2[].minPriceRp` | string |  |
| `perpProductsV2[].perpProductSubType` | string |  |
| `perpProductsV2[].pricePrecision` | number |  |
| `perpProductsV2[].priceScale` | number |  |
| `perpProductsV2[].qtyPrecision` | number |  |
| `perpProductsV2[].qtyStepSize` | string |  |
| `perpProductsV2[].quoteCurrency` | string |  |
| `perpProductsV2[].ratioScale` | number |  |
| `perpProductsV2[].settleCurrency` | string |  |
| `perpProductsV2[].status` | string |  |
| `perpProductsV2[].symbol` | string |  |
| `perpProductsV2[].tickSize` | string |  |
| `perpProductsV2[].tipOrderQty` | number |  |
| `perpProductsV2[].tipOrderQtyRq` | string |  |
| `perpProductsV2[].type` | string |  |
| `products[].code` | number |  |
| `products[].contractSize` | number |  |
| `products[].contractUnderlyingAssets` | string |  |
| `products[].defaultLeverage` | string |  |
| `products[].description` | string |  |
| `products[].displaySymbol` | string |  |
| `products[].fundingInterval` | number |  |
| `products[].fundingRate8hSymbol` | string |  |
| `products[].fundingRateSymbol` | string |  |
| `products[].indexSymbol` | string |  |
| `products[].leverageMargin` | number |  |
| `products[].listTime` | number |  |
| `products[].lotSize` | number |  |
| `products[].majorSymbol` | boolean |  |
| `products[].markSymbol` | string |  |
| `products[].maxLeverage` | number |  |
| `products[].maxOI` | number |  |
| `products[].maxOrderQty` | number |  |
| `products[].maxPriceEp` | number |  |
| `products[].minPriceEp` | number |  |
| `products[].pricePrecision` | number |  |
| `products[].priceScale` | number |  |
| `products[].quoteCurrency` | string |  |
| `products[].ratioScale` | number |  |
| `products[].settleCurrency` | string |  |
| `products[].status` | string |  |
| `products[].symbol` | string |  |
| `products[].tickSize` | number |  |
| `products[].tipOrderQty` | number |  |
| `products[].type` | string |  |
| `ratioScale` | number |  |
| `riskLimits[].riskLimits[].initialMargin` | string |  |
| `riskLimits[].riskLimits[].initialMarginEr` | number |  |
| `riskLimits[].riskLimits[].limit` | number |  |
| `riskLimits[].riskLimits[].maintenanceMargin` | string |  |
| `riskLimits[].riskLimits[].maintenanceMarginEr` | number |  |
| `riskLimits[].steps` | string |  |
| `riskLimits[].symbol` | string |  |
| `riskLimitsV2[].riskLimits[].initialMarginRr` | string |  |
| `riskLimitsV2[].riskLimits[].limit` | number |  |
| `riskLimitsV2[].riskLimits[].maintenanceMarginRr` | string |  |
| `riskLimitsV2[].steps` | string |  |
| `riskLimitsV2[].symbol` | string |  |

## Native endpoint

Through the native Phemex API, this operation is `GET /public/products` (base URL `https://api.phemex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

