# Alpha Vantage: Get Intraday Time Series

Retrieves intraday time series data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-intraday-time-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-intraday-time-series?connectionId=$CONNECTION_ID&interval=string&symbol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interval": "string",
  "symbol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-intraday-time-series?${params}`, {
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
| `interval` | string | yes | Query parameter $key for TIME_SERIES_INTRADAY. |
| `month` | string | no | Query parameter $key for TIME_SERIES_INTRADAY. |
| `outputsize` | string | no | Query parameter $key for TIME_SERIES_INTRADAY. |
| `symbol` | string | yes | Query parameter $key for TIME_SERIES_INTRADAY. |

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

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-intraday-time-series.md) for the provider-specific parameters and requirements.

