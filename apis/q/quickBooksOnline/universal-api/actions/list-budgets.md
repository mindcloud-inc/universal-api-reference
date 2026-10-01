# QuickBooks Online: List Budgets



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-budgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-budgets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-budgets?${params}`, {
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

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-budgets.md) for the provider-specific parameters and requirements.

