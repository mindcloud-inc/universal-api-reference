# Avaza: Get Timesheet Summary

Retrieves aggregated timesheet data from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-timesheet-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-timesheet-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-timesheet-summary?${params}`, {
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
| `modelGroupBy` | list<string> | no | (Optional) Combine one, two or three levels of Grouping. Combine these possible grouping values: "Customer", "Project", "Category", "User", "Task", "Year", "Month", "Day", "Week". |
| `modelEntryDateFrom` | date | no | (Required) Filter for timesheets greater or equal to the specified date. e.g. 2019-01-25. You can optionally include a time component, otherwise it assumes 00:00 |
| `modelEntryDateTo` | date | no | (Required) Filter for timesheets with an entry date smaller or equal to the specified date. e.g. 2019-01-25. You can optionally include a time component, otherwise it assumes 00:00 |
| `modelUserID` | list<number> | no | (Optional) Defaults to the current user. Provide one or more UserIDs of Users whose timesheets should be retrieved. If the current user doesn't have impersonation rights, then they will only see their own data. |
| `modelProjectID` | number | no | (Optional) Filter by Project |
| `modelIsBillable` | boolean | no | (Optional) Filter by the billable status of Timesheets. |
| `modelIsInvoiced` | boolean | no | (Optional) Filter for timesheets by whether they have been Invoiced or not. |
| `modelTimesheetEntryApprovalStatusCode` | list<string> | no | (Optional) Filter for timesheets that belong to one of the specified statuses (Draft, Pending, Approved, AutoApproved, Rejected) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/TimesheetSummary` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet-summary.md) for the provider-specific parameters and requirements.

