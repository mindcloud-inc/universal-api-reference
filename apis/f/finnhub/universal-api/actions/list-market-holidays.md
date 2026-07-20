# Finnhub: List Market Holidays

Retrieves market holidays from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-market-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-market-holidays?connectionId=$CONNECTION_ID&exchange=e.g.%20US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "e.g. US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-market-holidays?${params}`, {
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
| `exchange` | string | yes | Exchange code for market holidays, such as US. Example: `e.g. US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "atDate": "2026-05-07T12:00:00.000Z",
        "eventName": "Ava Chen",
        "postMarket": "string",
        "tradingHour": "string"
      },
      "exchange": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.atDate` | date |  |
| `data.eventName` | string |  |
| `data.postMarket` | string |  |
| `data.tradingHour` | string |  |
| `exchange` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/market-holiday` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-market-holidays.md) for the provider-specific parameters and requirements.

