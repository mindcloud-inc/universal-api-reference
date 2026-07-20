# Phemex Universal API Examples

These examples use the MindCloud API key and Phemex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products



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

Example response:

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

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phemex/latest/actions/list-products).
