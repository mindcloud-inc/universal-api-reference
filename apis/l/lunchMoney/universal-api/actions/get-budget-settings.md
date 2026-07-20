# Lunch Money: Get budget settings



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-settings?${params}`, {
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
      "budgetHideNoActivity": true,
      "budgetIncomeOption": "string",
      "budgetPeriodAnchorDate": "2026-05-07T12:00:00.000Z",
      "budgetPeriodGranularity": "string",
      "budgetPeriodQuantity": 1,
      "budgetRolloverLeftToBudget": true,
      "budgetUseLastDayOfMonth": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetHideNoActivity` | boolean |  |
| `budgetIncomeOption` | string |  |
| `budgetPeriodAnchorDate` | date |  |
| `budgetPeriodGranularity` | string |  |
| `budgetPeriodQuantity` | number |  |
| `budgetRolloverLeftToBudget` | boolean |  |
| `budgetUseLastDayOfMonth` | boolean |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /budgets/settings` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-budget-settings.md) for the provider-specific parameters and requirements.

