# Emporix Commerce Engine: Match Prices

Finds matching prices in Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/match-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/match-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/match-prices?${params}`, {
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
      "currency": "string",
      "effectiveValue": 1,
      "includesTax": true,
      "itemRef": {},
      "metadata": {},
      "originalValue": 1,
      "priceId": "string",
      "priceListId": "string",
      "priceModel": {},
      "salePrice": {},
      "tierValues": [
        {}
      ],
      "totalValue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `effectiveValue` | number |  |
| `includesTax` | boolean |  |
| `itemRef` | object |  |
| `metadata` | object |  |
| `originalValue` | number |  |
| `priceId` | string |  |
| `priceListId` | string |  |
| `priceModel` | object |  |
| `salePrice` | object |  |
| `tierValues` | array<object> |  |
| `totalValue` | number |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /price/{{credentials.tenantId}}/match-prices` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-prices.md) for the provider-specific parameters and requirements.

