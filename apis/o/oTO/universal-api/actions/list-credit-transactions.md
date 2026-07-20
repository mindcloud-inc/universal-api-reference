# OTO: List Credit Transactions

Retrieves credit transactions from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-credit-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-credit-transactions?connectionId=$CONNECTION_ID&minDate=2026-01-01&maxDate=2026-04-02" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "minDate": "2026-01-01",
  "maxDate": "2026-04-02"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-credit-transactions?${params}`, {
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
| `minDate` | date | yes | Earliest transaction date to include, in YYYY-MM-DD format. Default: `2026-01-01`. |
| `maxDate` | date | yes | Latest transaction date to include, in YYYY-MM-DD format. Default: `2026-04-02`. |
| `perPage` | number | no | Maximum number of transactions to return per page. Default: `10`. |
| `page` | number | no | Page number to fetch. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "transactions": [
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
| `success` | boolean |  |
| `transactions` | array<object> |  |

## Native endpoint

Through the native OTO API, this operation is `GET /creditTransactions` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-credit-transactions.md) for the provider-specific parameters and requirements.

