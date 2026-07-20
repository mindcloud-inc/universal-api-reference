# Finnhub: Get Basic Financials

Retrieves basic financials from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-basic-financials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-basic-financials?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-basic-financials?${params}`, {
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
      "metric": {},
      "metricType": "string",
      "series": {},
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metric` | object |  |
| `metricType` | string |  |
| `series` | object |  |
| `symbol` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/metric` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-basic-financials.md) for the provider-specific parameters and requirements.

