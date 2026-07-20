# Alpha Vantage: Get Earnings Calendar

Retrieves earnings calendar data from Alpha Vantage.

```
GET https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-earnings-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha Vantage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-earnings-calendar?connectionId=$CONNECTION_ID&horizon=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "horizon": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/get-earnings-calendar?${params}`, {
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
| `horizon` | string | yes | Query parameter $key for EARNINGS_CALENDAR. |
| `symbol` | string | no | Query parameter $key for EARNINGS_CALENDAR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Length": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Length` | number |  |

## Native endpoint

Through the native Alpha Vantage API, this operation is `GET /query` (base URL `https://www.alphavantage.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-earnings-calendar.md) for the provider-specific parameters and requirements.

