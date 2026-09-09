# Walmart: Get Promotional Prices

Retrieves a list of promotional prices for a single SKU.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-promotional-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-promotional-prices?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-promotional-prices?${params}`, {
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
| `sku` | string | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. This will be used by the seller in the XSD file to refer to each item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pricingList": {
        "pricing": [
          {
            "comparisonPriceType": "string",
            "currentPrice": {
              "perUnitValue": {
                "amount": 1,
                "currency": "string"
              },
              "uomType": "string",
              "value": {
                "amount": 1,
                "currency": "string"
              }
            },
            "currentPriceType": "string",
            "effectiveDate": "2026-05-07T12:00:00.000Z",
            "expirationDate": "2026-05-07T12:00:00.000Z",
            "priceDisplayCodes": {
              "isClearance": true,
              "isReducedPrice": true,
              "isRollback": true,
              "isStrikethrough": true,
              "submapType": "string"
            },
            "promoId": "string"
          }
        ],
        "replaceAll": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pricingList.pricing[].comparisonPriceType` | string |  |
| `pricingList.pricing[].currentPrice.perUnitValue.amount` | number |  |
| `pricingList.pricing[].currentPrice.perUnitValue.currency` | string |  |
| `pricingList.pricing[].currentPrice.uomType` | string |  |
| `pricingList.pricing[].currentPrice.value.amount` | number |  |
| `pricingList.pricing[].currentPrice.value.currency` | string |  |
| `pricingList.pricing[].currentPriceType` | string |  |
| `pricingList.pricing[].effectiveDate` | date |  |
| `pricingList.pricing[].expirationDate` | date |  |
| `pricingList.pricing[].priceDisplayCodes.isClearance` | boolean |  |
| `pricingList.pricing[].priceDisplayCodes.isReducedPrice` | boolean |  |
| `pricingList.pricing[].priceDisplayCodes.isRollback` | boolean |  |
| `pricingList.pricing[].priceDisplayCodes.isStrikethrough` | boolean |  |
| `pricingList.pricing[].priceDisplayCodes.submapType` | string |  |
| `pricingList.pricing[].promoId` | string |  |
| `pricingList.replaceAll` | boolean |  |

## Native endpoint

Through the native Walmart API, this operation is `GET v3/promo/sku/:sku` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-promotional-prices.md) for the provider-specific parameters and requirements.

