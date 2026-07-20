# Implisense: Get Company Financials Availability By Lookup

Finds available financial years in Implisense API by lookup.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability-by-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability-by-lookup?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability-by-lookup?${params}`, {
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
| `query` | string | yes | Known company text, for example a company name and city. |
| `name` | string | no | Official company name. |
| `city` | string | no | City of the company headquarters. |
| `active` | boolean | no | Return only companies that are still active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accruals": [
        1
      ],
      "balanceSheetTotal": [
        1
      ],
      "cashAndCashEquivalents": [
        1
      ],
      "currentAssets": [
        1
      ],
      "equity": [
        1
      ],
      "fixedAssets": [
        1
      ],
      "id": "string",
      "netIncome": [
        1
      ],
      "numberOfEmployees": [
        1
      ],
      "obligations": [
        1
      ],
      "receivables": [
        1
      ],
      "revenue": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accruals` | array<number> |  |
| `balanceSheetTotal` | array<number> |  |
| `cashAndCashEquivalents` | array<number> |  |
| `currentAssets` | array<number> |  |
| `equity` | array<number> |  |
| `fixedAssets` | array<number> |  |
| `id` | string |  |
| `netIncome` | array<number> |  |
| `numberOfEmployees` | array<number> |  |
| `obligations` | array<number> |  |
| `receivables` | array<number> |  |
| `revenue` | array<number> |  |

## Native endpoint

Through the native Implisense API, this operation is `POST /companies/financials/exists` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-financials-availability-by-lookup.md) for the provider-specific parameters and requirements.

