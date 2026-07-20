# Alpha Vantage: Get STOCH Indicator

Retrieves STOCH indicator data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-stoch-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-stoch-indicator?connectionId=$CONNECTION_ID&interval=string&symbol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interval": "string",
  "symbol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-stoch-indicator?${params}`, {
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
| `interval` | string | yes | Query parameter $key for STOCH. |
| `symbol` | string | yes | Query parameter $key for STOCH. |

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

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stoch-indicator.md) for the provider-specific parameters and requirements.

