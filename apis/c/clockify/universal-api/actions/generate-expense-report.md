# Clockify: Generate Expense Report

Generates an expense report in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-expense-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-expense-report?connectionId=$CONNECTION_ID&dateRangeEnd=string&dateRangeStart=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateRangeEnd": "string",
  "dateRangeStart": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-expense-report?${params}`, {
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
| `approvalState` | list | no | One of: `ALL`, `APPROVED`, `UNAPPROVED`. |
| `billable` | boolean | no |  |
| `categories` | object | no |  |
| `categories.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `categories.ids[]` | array<string> | no |  |
| `categories.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `clients` | object | no |  |
| `clients.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `clients.ids[]` | array<string> | no |  |
| `clients.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `currency` | object | no |  |
| `currency.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `currency.ids[]` | array<string> | no |  |
| `currency.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `dateRangeEnd` | string | yes |  |
| `dateRangeStart` | string | yes |  |
| `dateRangeType` | list | no | One of: `ABSOLUTE`, `LAST_MONTH`, `LAST_WEEK`, `LAST_YEAR`, `PAST_TWO_WEEKS`, `THIS_MONTH`, `THIS_WEEK`, `THIS_YEAR`, `TODAY`, `YESTERDAY`. |
| `exportType` | list | no | One of: `CSV`, `JSON`, `JSON_V1`, `PDF`, `XLSX`, `ZIP`. |
| `invoicingState` | list | no | One of: `ALL`, `INVOICED`, `UNINVOICED`. |
| `note` | string | no |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `projects` | object | no |  |
| `projects.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `projects.ids[]` | array<string> | no |  |
| `projects.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `sortColumn` | list | no | One of: `AMOUNT`, `CATEGORY`, `DATE`, `ID`, `PROJECT`, `USER`. |
| `sortOrder` | list | no | One of: `ASCENDING`, `DESCENDING`. |
| `tasks` | object | no |  |
| `tasks.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `tasks.ids[]` | array<string> | no |  |
| `tasks.status` | list | no | One of: `ACTIVE`, `ALL`, `ARCHIVED`. |
| `timeZone` | string | no |  |
| `userGroups` | object | no |  |
| `userGroups.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `userLocale` | string | no |  |
| `users` | object | no |  |
| `users.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `users.ids[]` | array<string> | no |  |
| `users.status` | list | no | One of: `ACTIVE`, `ACTIVE_WITH_PENDING`, `ALL`, `INACTIVE`, `PENDING`. |
| `weekStart` | list | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `withoutNote` | boolean | no |  |
| `workspaceId` | list<string> | yes |  |
| `zoomLevel` | list | no | One of: `MONTH`, `WEEK`, `YEAR`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expenses": [
        [
          {}
        ]
      ],
      "totals": {
        "expensesCount": 1,
        "totalAmount": 1,
        "totalAmountBillable": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expenses[]` | array<object> |  |
| `expenses[].amount` | number |  |
| `expenses[].approvalRequestId` | string |  |
| `expenses[].billable` | boolean |  |
| `expenses[].categoryHasUnitPrice` | boolean |  |
| `expenses[].categoryId` | string |  |
| `expenses[].categoryName` | string |  |
| `expenses[].categoryUnit` | string |  |
| `expenses[].date` | string |  |
| `expenses[].exportFields[]` | array<string> |  |
| `expenses[].fileId` | string |  |
| `expenses[].fileName` | string |  |
| `expenses[].id` | string |  |
| `expenses[].invoicingInfo` | object |  |
| `expenses[].invoicingInfo.invoiceId` | string |  |
| `expenses[].invoicingInfo.manuallyInvoiced` | boolean |  |
| `expenses[].locked` | boolean |  |
| `expenses[].notes` | string |  |
| `expenses[].projectColor` | string |  |
| `expenses[].projectId` | string |  |
| `expenses[].projectName` | string |  |
| `expenses[].quantity` | number |  |
| `expenses[].reportName` | string |  |
| `expenses[].time` | string |  |
| `expenses[].userEmail` | string |  |
| `expenses[].userId` | string |  |
| `expenses[].userName` | string |  |
| `expenses[].userStatus` | string |  |
| `expenses[].workspaceId` | string |  |
| `totals` | object |  |
| `totals.expensesCount` | number |  |
| `totals.totalAmount` | number |  |
| `totals.totalAmountBillable` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/expenses/detailed` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-expense-report.md) for the provider-specific parameters and requirements.

