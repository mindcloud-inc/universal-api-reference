# Implisense: Get Company Financials Availability

Retrieves available financial years from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials-availability?${params}`, {
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
| `id` | string | yes | Implisense company identifier, for example DEVFCLQFW054. |

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

Through the native Implisense API, this operation is `GET /companies/:id/financials/exists` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-financials-availability.md) for the provider-specific parameters and requirements.

