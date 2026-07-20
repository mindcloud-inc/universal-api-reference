# Alpha Vantage: Get Forex Intraday

Retrieves forex intraday data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-forex-intraday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-forex-intraday?connectionId=$CONNECTION_ID&from_symbol=string&to_symbol=string&fromSymbol=e.g.%20EUR&toSymbol=e.g.%20USD&interval=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from_symbol": "string",
  "to_symbol": "string",
  "fromSymbol": "e.g. EUR",
  "toSymbol": "e.g. USD",
  "interval": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-forex-intraday?${params}`, {
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
| `from_symbol` | string | yes | Query parameter $key for FX_INTRADAY. |
| `outputsize` | string | no | Query parameter $key for FX_INTRADAY. |
| `to_symbol` | string | yes | Query parameter $key for FX_INTRADAY. |
| `fromSymbol` | string | yes | Base currency symbol. Example: `e.g. EUR`. |
| `toSymbol` | string | yes | Quote currency symbol. Example: `e.g. USD`. |
| `interval` | string | yes | Query parameter $key for FX_INTRADAY. One of: `0`, `1`, `2`, `3`, `4`. |

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

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forex-intraday.md) for the provider-specific parameters and requirements.

