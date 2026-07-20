# Financial Modeling Prep: Get Shares Float

Retrieves shares float data from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-shares-float
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-shares-float?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-shares-float?${params}`, {
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
| `symbol` | string | yes | Stock ticker symbol, such as AAPL. Example: `AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "floatShares": 1,
      "freeFloat": 1,
      "outstandingShares": 1,
      "source": "string",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `floatShares` | number |  |
| `freeFloat` | number |  |
| `outstandingShares` | number |  |
| `source` | string |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /shares-float` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shares-float.md) for the provider-specific parameters and requirements.

