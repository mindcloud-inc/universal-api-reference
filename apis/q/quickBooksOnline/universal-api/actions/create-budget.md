# QuickBooks Online: Create Budget



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "budgetType": "ProfitAndLoss",
  "budgetEntryType": "Monthly"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z",
    "budgetType": "ProfitAndLoss",
    "budgetEntryType": "Monthly"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Budget name. |
| `startDate` | date | yes | Budget start date. |
| `endDate` | date | yes | Budget end date. |
| `budgetType` | string | yes | QuickBooks budget type. Production proof used ProfitAndLoss. Default: `ProfitAndLoss`. |
| `budgetEntryType` | string | yes | QuickBooks budget entry cadence. Production proof used Monthly. Default: `Monthly`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | no | Whether the budget is active. Default: `true`. |

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

Through the native QuickBooks Online API, this operation is `POST /budget` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-budget.md) for the provider-specific parameters and requirements.

