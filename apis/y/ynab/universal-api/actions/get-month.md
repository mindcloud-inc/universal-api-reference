# YNAB: Get Month

Retrieves a month from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month?connectionId=$CONNECTION_ID&planId=string&month=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "month": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used. |
| `month` | string | yes | The budget month in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": 1,
      "activityCurrency": 1,
      "activityFormatted": "string",
      "ageOfMoney": 1,
      "budgeted": 1,
      "budgetedCurrency": 1,
      "budgetedFormatted": "string",
      "categories": [
        {}
      ],
      "deleted": true,
      "income": 1,
      "incomeCurrency": 1,
      "incomeFormatted": "string",
      "month": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "toBeBudgeted": 1,
      "toBeBudgetedCurrency": 1,
      "toBeBudgetedFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity` | number | The total activity for the month in milliunits. |
| `activityCurrency` | number | The currency-adjusted activity amount for the month in milliunits. |
| `activityFormatted` | string | The formatted activity amount for the month. |
| `ageOfMoney` | number | The age of money metric for the month. |
| `budgeted` | number | The total budgeted amount for the month in milliunits. |
| `budgetedCurrency` | number | The currency-adjusted budgeted amount for the month in milliunits. |
| `budgetedFormatted` | string | The formatted budgeted amount for the month. |
| `categories` | array<object> | The month category rows. |
| `deleted` | boolean | Whether the month record has been deleted. |
| `income` | number | The total income for the month in milliunits. |
| `incomeCurrency` | number | The currency-adjusted income amount for the month in milliunits. |
| `incomeFormatted` | string | The formatted income amount for the month. |
| `month` | date | The month represented by this detailed budget view. |
| `note` | string | The month note, when present. |
| `toBeBudgeted` | number | The amount still available to budget in milliunits. |
| `toBeBudgetedCurrency` | number | The currency-adjusted amount still available to budget in milliunits. |
| `toBeBudgetedFormatted` | string | The formatted amount still available to budget. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/months/:month` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-month.md) for the provider-specific parameters and requirements.

