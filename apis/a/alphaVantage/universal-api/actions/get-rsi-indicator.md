# Alpha Vantage: Get RSI Indicator

Retrieves RSI indicator data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-rsi-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-rsi-indicator?connectionId=$CONNECTION_ID&series_type=string&time_period=string&symbol=e.g.%20IBM&interval=0&timePeriod=e.g.%2014&seriesType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "series_type": "string",
  "time_period": "string",
  "symbol": "e.g. IBM",
  "interval": "0",
  "timePeriod": "e.g. 14",
  "seriesType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-rsi-indicator?${params}`, {
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
| `series_type` | string | yes | Query parameter $key for RSI. |
| `time_period` | string | yes | Query parameter $key for RSI. |
| `symbol` | string | yes | Query parameter $key for RSI. Example: `e.g. IBM`. |
| `interval` | string | yes | Query parameter $key for RSI. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `timePeriod` | string | yes | Number of data points to evaluate. Example: `e.g. 14`. |
| `seriesType` | string | yes | Price series to use. One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Information": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Information` | string |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rsi-indicator.md) for the provider-specific parameters and requirements.

