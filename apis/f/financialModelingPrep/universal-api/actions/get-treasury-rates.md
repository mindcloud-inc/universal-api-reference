# Financial Modeling Prep: Get Treasury Rates

Retrieves treasury rates from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-treasury-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-treasury-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-treasury-rates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "month1": 1,
      "month2": 1,
      "month3": 1,
      "month6": 1,
      "year1": 1,
      "year10": 1,
      "year30": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `month1` | number |  |
| `month2` | number |  |
| `month3` | number |  |
| `month6` | number |  |
| `year1` | number |  |
| `year10` | number |  |
| `year30` | number |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /treasury-rates` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-treasury-rates.md) for the provider-specific parameters and requirements.

