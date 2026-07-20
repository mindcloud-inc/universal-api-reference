# YNAB: Get Month Category

Retrieves a category for a specific month in YNAB.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month-category?connectionId=$CONNECTION_ID&planId=string&month=string&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "month": "string",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-month-category?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used or default when enabled. |
| `month` | string | yes | The plan month in YYYY-MM-DD format or current. |
| `categoryId` | string | yes | The id of the category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": 1,
      "activityCurrency": 1,
      "activityFormatted": "string",
      "balance": 1,
      "balanceCurrency": 1,
      "balanceFormatted": "string",
      "budgeted": 1,
      "budgetedCurrency": 1,
      "budgetedFormatted": "string",
      "categoryGroupId": "string",
      "categoryGroupName": "Ava Chen",
      "deleted": true,
      "goalCadence": 1,
      "goalCadenceFrequency": 1,
      "goalCreationMonth": "2026-05-07T12:00:00.000Z",
      "goalDay": 1,
      "goalMonthsToBudget": 1,
      "goalNeedsWholeAmount": true,
      "goalOverallFunded": 1,
      "goalOverallFundedCurrency": 1,
      "goalOverallFundedFormatted": "string",
      "goalOverallLeft": 1,
      "goalOverallLeftCurrency": 1,
      "goalOverallLeftFormatted": "string",
      "goalPercentageComplete": 1,
      "goalSnoozedAt": "2026-05-07T12:00:00.000Z",
      "goalTarget": 1,
      "goalTargetCurrency": 1,
      "goalTargetDate": "2026-05-07T12:00:00.000Z",
      "goalTargetFormatted": "string",
      "goalTargetMonth": "2026-05-07T12:00:00.000Z",
      "goalType": "string",
      "goalUnderFunded": 1,
      "goalUnderFundedCurrency": 1,
      "goalUnderFundedFormatted": "string",
      "hidden": true,
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "originalCategoryGroupId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity` | number | The activity amount in milliunits. |
| `activityCurrency` | number | The currency-adjusted activity amount in milliunits. |
| `activityFormatted` | string | The formatted activity amount. |
| `balance` | number | The category balance in milliunits. |
| `balanceCurrency` | number | The currency-adjusted category balance in milliunits. |
| `balanceFormatted` | string | The formatted category balance. |
| `budgeted` | number | The budgeted amount in milliunits. |
| `budgetedCurrency` | number | The currency-adjusted budgeted amount in milliunits. |
| `budgetedFormatted` | string | The formatted budgeted amount. |
| `categoryGroupId` | string | The parent category group ID. |
| `categoryGroupName` | string | The parent category group name. |
| `deleted` | boolean | Whether the category has been deleted. |
| `goalCadence` | number | The goal cadence, when present. |
| `goalCadenceFrequency` | number | The goal cadence frequency, when present. |
| `goalCreationMonth` | date | The month the goal was created, when present. |
| `goalDay` | number | The goal day, when present. |
| `goalMonthsToBudget` | number | The remaining months to budget, when present. |
| `goalNeedsWholeAmount` | boolean | Whether the goal requires the full amount. |
| `goalOverallFunded` | number | The overall funded amount in milliunits, when present. |
| `goalOverallFundedCurrency` | number | The currency-adjusted overall funded amount in milliunits, when present. |
| `goalOverallFundedFormatted` | string | The formatted overall funded amount, when present. |
| `goalOverallLeft` | number | The remaining amount left toward the goal in milliunits, when present. |
| `goalOverallLeftCurrency` | number | The currency-adjusted remaining goal amount in milliunits, when present. |
| `goalOverallLeftFormatted` | string | The formatted remaining goal amount, when present. |
| `goalPercentageComplete` | number | The percentage complete for the goal, when present. |
| `goalSnoozedAt` | date | When the goal was snoozed, when present. |
| `goalTarget` | number | The goal target amount in milliunits. |
| `goalTargetCurrency` | number | The currency-adjusted goal target amount in milliunits. |
| `goalTargetDate` | date | The target date for the goal, when present. |
| `goalTargetFormatted` | string | The formatted goal target amount. |
| `goalTargetMonth` | date | The target month for the goal, when present. |
| `goalType` | string | The goal type, when present. |
| `goalUnderFunded` | number | The underfunded amount in milliunits, when present. |
| `goalUnderFundedCurrency` | number | The currency-adjusted underfunded amount in milliunits, when present. |
| `goalUnderFundedFormatted` | string | The formatted underfunded amount, when present. |
| `hidden` | boolean | Whether the category is hidden. |
| `id` | string | The YNAB category ID. |
| `name` | string | The category name. |
| `note` | string | The category note, when present. |
| `originalCategoryGroupId` | string | The original category group ID, when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/months/:month/categories/:categoryId` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-month-category.md) for the provider-specific parameters and requirements.

