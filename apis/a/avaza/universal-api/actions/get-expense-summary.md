# Avaza: Get Expense Summary

Retrieves aggregated expense data from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-expense-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-expense-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-expense-summary?${params}`, {
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
| `modelGroupBy` | list<string> | no | (Optional) Combine one, two or three levels of Grouping. Combine these possible grouping values: "Category", "ChargeableStatus", "Merchant", "ApprovalStatus", "ReimbursementStatus", "Customer", "Project", "User", "Task", "Year", "Month", "Day", "Week". |
| `modelExpenseDateFrom` | date | no | (Required) Filter for expenses with expense dates greater or equal to the specified date. e.g. 2019-01-25. |
| `modelExpenseDateTo` | date | no | (Required) Filter for expenses with an expense date smaller or equal to the specified date. e.g. 2019-01-25. |
| `modelUserID` | list<number> | no | (Optional) Defaults to the current user. Provide one or more UserIDs of Users whose expenses should be retrieved. If the current user doesn't have impersonation rights, then they will only see their own data. |
| `modelProjectID` | number | no | (Optional) Filter by Project |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/ExpenseSummary` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense-summary.md) for the provider-specific parameters and requirements.

