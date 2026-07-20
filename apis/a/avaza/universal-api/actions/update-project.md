# Avaza: Update Project

Updates an existing project in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldstoupdate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldstoupdate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectid` | number | no | The ID of the Project to update |
| `fieldstoupdate` | list<string> | yes |  |
| `projecttitle` | string | no | (optional) An updated project title. (255 characters max) |
| `projectnotes` | string | no | (optional) Any descriptive notes about the project. (2000 characters max) |
| `timesheetapprovalrequiredbydefault` | boolean | no | Whether timesheet approval should be required by default for newly added project members. |
| `istaskrequiredontimesheet` | boolean | no | Whether timesheets entered against this project require a task to be selected. |
| `startdate` | date | no |  |
| `enddate` | date | no |  |
| `budgetamount` | number | no |  |
| `budgethours` | number | no |  |
| `projectstatuscode` | string | no | Update the project status (string, optional): (Possible values: NotStarted, InProgress, Complete, OnHold) |
| `projectcategoryidfk` | number | no |  |
| `projectbillabletypecode` | string | no | The billing method of the project. (string, optional) Possible values: CategoryHourly, NoRate, NotBillable, PersonHourly, ProjectHourly |
| `projectbudgettypecode` | string | no | The project budgeting type. (string, optional) Possible values: NoBudget, PersonHours, ProjectFees, ProjectHours, CategoryHours |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `PUT /api/Project` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

