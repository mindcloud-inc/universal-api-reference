# Finnhub: Get Price Target

Retrieves a price target from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-price-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-price-target?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-price-target?${params}`, {
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
| `symbol` | string | yes | Company symbol, such as AAPL. Example: `e.g. AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "symbol": "string",
      "targetHigh": 1,
      "targetLow": 1,
      "targetMean": 1,
      "targetMedian": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastUpdated` | date |  |
| `symbol` | string |  |
| `targetHigh` | number |  |
| `targetLow` | number |  |
| `targetMean` | number |  |
| `targetMedian` | number |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/price-target` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price-target.md) for the provider-specific parameters and requirements.

