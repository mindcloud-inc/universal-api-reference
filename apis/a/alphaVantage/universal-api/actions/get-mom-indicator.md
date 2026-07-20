# Alpha Vantage: Get MOM Indicator

Retrieves MOM indicator data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-mom-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-mom-indicator?connectionId=$CONNECTION_ID&interval=string&series_type=string&symbol=string&time_period=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interval": "string",
  "series_type": "string",
  "symbol": "string",
  "time_period": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-mom-indicator?${params}`, {
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
| `interval` | string | yes | Query parameter $key for MOM. |
| `series_type` | string | yes | Query parameter $key for MOM. |
| `symbol` | string | yes | Query parameter $key for MOM. |
| `time_period` | string | yes | Query parameter $key for MOM. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Meta Data": {},
      "Technical Analysis: MOM": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Meta Data` | object |  |
| `Technical Analysis: MOM` | object |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mom-indicator.md) for the provider-specific parameters and requirements.

