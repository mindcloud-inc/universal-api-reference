# Finnhub: List Earnings Surprises

Retrieves earnings surprises from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-surprises
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-surprises?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-surprises?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Optional number of earnings surprise records to return. Example: `e.g. 10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": 1,
      "estimate": 1,
      "period": "2026-05-07T12:00:00.000Z",
      "quarter": 1,
      "surprise": 1,
      "surprisePercent": 1,
      "symbol": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | number |  |
| `estimate` | number |  |
| `period` | date |  |
| `quarter` | number |  |
| `surprise` | number |  |
| `surprisePercent` | number |  |
| `symbol` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/earnings` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-earnings-surprises.md) for the provider-specific parameters and requirements.

