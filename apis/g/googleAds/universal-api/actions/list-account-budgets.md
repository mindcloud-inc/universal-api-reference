# Google Ads: List Account Budgets

Retrieves account budgets from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-budgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-budgets?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20account_budget.id%2C%20account_budget.status%20FROM%20account_budget%20LIMIT%2050" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT account_budget.id, account_budget.status FROM account_budget LIMIT 50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-budgets?${params}`, {
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
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query to list account budget resources. Default: `SELECT account_budget.id, account_budget.name, account_budget.status, account_budget.amount_served_micros FROM account_budget ORDER BY account_budget.id DESC LIMIT 50`. Example: `SELECT account_budget.id, account_budget.status FROM account_budget LIMIT 50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldMask": "string",
      "queryResourceConsumption": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldMask` | string |  |
| `queryResourceConsumption` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-budgets.md) for the provider-specific parameters and requirements.

