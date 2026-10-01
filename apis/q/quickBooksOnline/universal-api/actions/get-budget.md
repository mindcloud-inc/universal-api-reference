# QuickBooks Online: Get Budget



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-budget?connectionId=$CONNECTION_ID&budgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "budgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-budget?${params}`, {
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
| `budgetId` | string | yes | QuickBooks budget ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "BudgetDetail": [
        {}
      ],
      "BudgetEntryType": "string",
      "BudgetType": "string",
      "EndDate": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "Name": "Ava Chen",
      "StartDate": "2026-05-07T12:00:00.000Z",
      "SyncToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean | Whether the budget is active. |
| `BudgetDetail` | array<object> | Budget detail rows when returned by QuickBooks. |
| `BudgetEntryType` | string | Budget entry cadence, such as Monthly. |
| `BudgetType` | string | Budget type, such as ProfitAndLoss. |
| `EndDate` | date | Budget end date. |
| `Id` | string | QuickBooks budget ID. |
| `Name` | string | Budget name. |
| `StartDate` | date | Budget start date. |
| `SyncToken` | string | QuickBooks sync token for updates. |

## Native endpoint

Through the native QuickBooks Online API, this operation is `GET /budget/:budgetId` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-budget.md) for the provider-specific parameters and requirements.

