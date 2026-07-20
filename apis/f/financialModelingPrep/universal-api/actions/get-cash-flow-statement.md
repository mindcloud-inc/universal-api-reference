# Financial Modeling Prep: Get Cash Flow Statement

Retrieves cash flow statements from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-cash-flow-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-cash-flow-statement?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-cash-flow-statement?${params}`, {
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
      "capitalExpenditure": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "fiscalYear": "string",
      "freeCashFlow": 1,
      "netIncome": 1,
      "operatingCashFlow": 1,
      "period": "string",
      "reportedCurrency": "string",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capitalExpenditure` | number |  |
| `date` | date |  |
| `fiscalYear` | string |  |
| `freeCashFlow` | number |  |
| `netIncome` | number |  |
| `operatingCashFlow` | number |  |
| `period` | string |  |
| `reportedCurrency` | string |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /cash-flow-statement` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cash-flow-statement.md) for the provider-specific parameters and requirements.

