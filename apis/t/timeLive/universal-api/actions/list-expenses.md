# TimeLive: List Expenses

Retrieves all expense records from TimeLive.

```
GET https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeLive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-expenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-expenses?${params}`, {
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
      "AccountExpenseId": 1,
      "AccountExpenseName": "Ava Chen",
      "AccountExpenseTypeId": 1,
      "DefaultExpenseRate": 1,
      "DisabledEditingOfRate": "string",
      "ExpenseType": "string",
      "IsBillable": "string",
      "IsDisabled": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountExpenseId` | number |  |
| `AccountExpenseName` | string |  |
| `AccountExpenseTypeId` | number |  |
| `DefaultExpenseRate` | number |  |
| `DisabledEditingOfRate` | string |  |
| `ExpenseType` | string |  |
| `IsBillable` | string |  |
| `IsDisabled` | string |  |

## Native endpoint

Through the native TimeLive API, this operation is `GET /Expenses` (base URL `https://mindcloudtl.livetecs.com/classic/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

