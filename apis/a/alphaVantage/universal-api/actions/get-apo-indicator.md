# Alpha Vantage: Get APO Indicator

Retrieves APO indicator data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-apo-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-apo-indicator?connectionId=$CONNECTION_ID&fastperiod=string&interval=string&matype=string&series_type=string&symbol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fastperiod": "string",
  "interval": "string",
  "matype": "string",
  "series_type": "string",
  "symbol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-apo-indicator?${params}`, {
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
| `fastperiod` | string | yes | Query parameter $key for APO. |
| `interval` | string | yes | Query parameter $key for APO. |
| `matype` | string | yes | Query parameter $key for APO. |
| `series_type` | string | yes | Query parameter $key for APO. |
| `symbol` | string | yes | Query parameter $key for APO. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Meta Data": {},
      "Technical Analysis: APO": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Meta Data` | object |  |
| `Technical Analysis: APO` | object |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-apo-indicator.md) for the provider-specific parameters and requirements.

