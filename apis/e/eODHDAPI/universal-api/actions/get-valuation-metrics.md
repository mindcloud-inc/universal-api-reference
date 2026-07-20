# EODHD: Get Valuation Metrics

Retrieves valuation metrics for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-valuation-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-valuation-metrics?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-valuation-metrics?${params}`, {
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
| `symbol` | string | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. Example: `AAPL.US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EnterpriseValue": 1,
      "EnterpriseValueEbitda": 1,
      "EnterpriseValueRevenue": 1,
      "ForwardPE": 1,
      "PriceBookMRQ": 1,
      "PriceSalesTTM": 1,
      "TrailingPE": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EnterpriseValue` | number | Enterprise value. |
| `EnterpriseValueEbitda` | number | Enterprise value to EBITDA. |
| `EnterpriseValueRevenue` | number | Enterprise value to revenue. |
| `ForwardPE` | number | Forward PE ratio. |
| `PriceBookMRQ` | number | Price-to-book ratio. |
| `PriceSalesTTM` | number | Price-to-sales ratio. |
| `TrailingPE` | number | Trailing PE ratio. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-valuation-metrics.md) for the provider-specific parameters and requirements.

