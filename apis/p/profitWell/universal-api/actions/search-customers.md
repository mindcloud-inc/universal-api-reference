# ProfitWell: Search Customers

Finds customers in ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/search-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/search-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/search-customers?${params}`, {
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
| `startDate` | string | no | Get customers who have been updated on or after this date. |
| `endDate` | string | no | Get customers who have been updated before this date. |
| `email` | string | no | Filter customers by email. |
| `direction` | list | no | Order the results ascending or descending. One of: `asc`, `desc`. Default: `asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated_on": "string",
      "churned_on": "string",
      "created_on": "string",
      "customer_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "mrr_cents": 1,
      "plans": [
        "string"
      ],
      "status": "string",
      "total_spend_cents": 1,
      "updated_on": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated_on` | string | When the customer was activated. |
| `churned_on` | string | When the customer churned, if applicable. |
| `created_on` | string | When the customer record was created. |
| `customer_id` | string | The ProfitWell customer identifier. |
| `email` | string | The customer email address. |
| `first_name` | string | The customer's first name. |
| `last_name` | string | The customer's last name. |
| `mrr_cents` | number | The customer's MRR in cents. |
| `plans` | array<string> | Plan names associated with the customer. |
| `status` | string | The customer status. |
| `total_spend_cents` | number | Total customer spend in cents. |
| `updated_on` | string | When the customer was last updated. |

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/customers/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-customers.md) for the provider-specific parameters and requirements.

