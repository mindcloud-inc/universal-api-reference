# ProfitWell: List Retain Unsubscribed Customers

Retrieves Retain unsubscribed customers from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/list-retain-unsubscribed-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/list-retain-unsubscribed-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&interventionType=reactivation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "interventionType": "reactivation"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/list-retain-unsubscribed-customers?${params}`, {
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
| `interventionType` | list | yes | Must be either term_optimization or reactivation. One of: `reactivation`, `term_optimization`. |
| `startDate` | string | no | Get customers who unsubscribed on this date or later. |
| `endDate` | string | no | Get customers who unsubscribed on this date or before. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/retain/unsubscribed_customers/:intervention_type/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-retain-unsubscribed-customers.md) for the provider-specific parameters and requirements.

