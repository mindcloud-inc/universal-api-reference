# Implisense: Get Company Financials

Retrieves company financials from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-financials?${params}`, {
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
        {}
      ],
      "balanceSheetTotal": [
        {}
      ],
      "cashAndCashEquivalents": [
        {}
      ],
      "currentAssets": [
        {}
      ],
      "equity": [
        {}
      ],
      "fixedAssets": [
        {}
      ],
      "id": "string",
      "netIncome": [
        {}
      ],
      "numberOfEmployees": [
        {}
      ],
      "obligations": [
        {}
      ],
      "receivables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accruals` | array<object> |  |
| `balanceSheetTotal` | array<object> |  |
| `cashAndCashEquivalents` | array<object> |  |
| `currentAssets` | array<object> |  |
| `equity` | array<object> |  |
| `fixedAssets` | array<object> |  |
| `id` | string |  |
| `netIncome` | array<object> |  |
| `numberOfEmployees` | array<object> |  |
| `obligations` | array<object> |  |
| `receivables` | array<object> |  |

## Native endpoint

Through the native Implisense API, this operation is `GET /companies/:id/financials` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-financials.md) for the provider-specific parameters and requirements.

