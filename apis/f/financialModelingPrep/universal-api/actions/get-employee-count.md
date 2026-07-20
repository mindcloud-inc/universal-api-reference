# Financial Modeling Prep: Get Employee Count

Retrieves employee count data from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-employee-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-employee-count?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-employee-count?${params}`, {
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
      "cik": "string",
      "companyName": "Ava Chen",
      "employeeCount": 1,
      "filingDate": "2026-05-07T12:00:00.000Z",
      "periodOfReport": "2026-05-07T12:00:00.000Z",
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
| `cik` | string |  |
| `companyName` | string |  |
| `employeeCount` | number |  |
| `filingDate` | date |  |
| `periodOfReport` | date |  |
| `source` | string |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /employee-count` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-count.md) for the provider-specific parameters and requirements.

