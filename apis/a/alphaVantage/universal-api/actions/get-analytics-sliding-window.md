# Alpha Vantage: Get Analytics Sliding Window

Retrieves analytics sliding window data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-analytics-sliding-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-analytics-sliding-window?connectionId=$CONNECTION_ID&CALCULATIONS=string&INTERVAL=string&OHLC=string&RANGE=string&SYMBOLS=string&WINDOW_SIZE=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "CALCULATIONS": "string",
  "INTERVAL": "string",
  "OHLC": "string",
  "RANGE": "string",
  "SYMBOLS": "string",
  "WINDOW_SIZE": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-analytics-sliding-window?${params}`, {
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
| `CALCULATIONS` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |
| `INTERVAL` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |
| `OHLC` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |
| `RANGE` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |
| `SYMBOLS` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |
| `WINDOW_SIZE` | string | yes | Query parameter $key for ANALYTICS_SLIDING_WINDOW. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-sliding-window.md) for the provider-specific parameters and requirements.

