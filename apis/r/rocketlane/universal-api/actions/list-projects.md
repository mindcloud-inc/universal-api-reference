# Rocketlane: List Projects

Lists projects in Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-projects?${params}`, {
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
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | string | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocatedHours": 1,
      "allocatedMinutes": 1,
      "annualizedRecurringRevenue": 1,
      "archived": true,
      "autoAllocation": true,
      "billableHours": 1,
      "billableMinutes": 1,
      "budgetedHours": 1,
      "createdAt": 1,
      "createdBy": {},
      "currency": "string",
      "currentPhases": [
        {}
      ],
      "customer": {},
      "customersInvited": 1,
      "customersJoined": 1,
      "dueDate": "string",
      "dueDateActual": "string",
      "externalReferenceId": "string",
      "fields": [
        {}
      ],
      "financials": {},
      "inferredProgress": "string",
      "nonBillableHours": 1,
      "nonBillableMinutes": 1,
      "owner": {},
      "partnerCompanies": [
        {}
      ],
      "percentageBudgetConsumed": 1,
      "percentageBudgetedHoursConsumed": 1,
      "plannedDurationInDays": 1,
      "progressPercentage": 1,
      "projectAgeInDays": 1,
      "projectFee": 1,
      "projectId": 1,
      "projectName": "Ava Chen",
      "remainingHours": 1,
      "remainingMinutes": 1,
      "sources": [
        {}
      ],
      "startDate": "string",
      "startDateActual": "string",
      "status": {},
      "teamMembers": {},
      "trackedHours": 1,
      "trackedMinutes": 1,
      "updatedAt": 1,
      "updatedBy": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedHours` | number | If the project has `allocations` against say users or placeholders, it is collected and computed in hours. |
| `allocatedMinutes` | number | If the project has `allocations` against say users or placeholders, it is collected and computed in minutes. |
| `annualizedRecurringRevenue` | number | Indicates the value of the recurring revenue of the customer's subscriptions for a single calendar year. |
| `archived` | boolean | The field `archived` denotes whether the project is archived or not. If the project is archived, there's an option to un-archive the project. |
| `autoAllocation` | boolean | The field autoAllocation defines whether Auto Allocation is enabled for the project or not. If auto allocation is enabled, instead of adding it manually, the allocations are computed from the tasks duration, effort and the assignees specified in the project. |
| `billableHours` | number | If the project has time entries tracked under billable, it is collected and computed in hours. |
| `billableMinutes` | number | If the project has time entries tracked under billable, it is collected and computed in minutes. |
| `budgetedHours` | number | Budgeted hours represent the total hours allocated for project execution. This value can be edited at any point throughout the project's duration. You can enter the budgeted hours in decimal form, including both hours and minutes, with up to two decimal places of precision. Eg: 1.65 hrs = 1h 39m(1.65h * 60m = 99m). |
| `createdAt` | number | The time when the project was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who created the project. |
| `currency` | string | The currency for handling the project’s financials. You can only specify a currency for a project that is added at the account level. Please note that the project’s currency cannot to changed once set. |
| `currentPhases` | array<object> | The phases that are currently marked as in progress are available here. |
| `customer` | object | Company details for the invoice |
| `customersInvited` | number | Reflects the number of customers that have been invited to the project. |
| `customersJoined` | number | CustomersJoined tracks the actual number of customers who joined the project after being invited. It is mostly used to track customer engagement. |
| `dueDate` | string | The day on which the project's execution is planned to be completed. The due date is not required and can be left blank. If sources (templates) are included as part of the project creation, the project's due date will be calculated depending on the duration of the specified sources. For projects where both startDate and dueDate are specified, the latter must be on or after the given startDate. The format for the due date is _YYYY-MM-DD_. |
| `dueDateActual` | string | The date when project status gets changed to completed. The status can be either the default provided status (completed) or a custom status that is labelled under the Completed category.  It will be null if the project is yet to be completed. The format for the actual due date is _YYYY-MM-DD_. |
| `externalReferenceId` | string | An externalReferenceId is a unique identifier that links entities or transactions between external systems and Rocketlane, ensuring accurate data correlation and consistency. |
| `fields` | array<object> | Fields lists the custom project fields whose values were provided during project creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
| `financials` | object | This section addresses the financial aspects of the projects and the associated fields. |
| `inferredProgress` | string | The `inferredProgress` can be used to know whether the project's progress is as per the expectation. For eg: the value `ON_TRACK` specifies that the project is in good state and not further action would be necessary to track the progress of it, whereas the value `RUNNING_LATE` means that the project state deviates from the original plan and needs immediate attention. |
| `nonBillableHours` | number | If the project has time entries tracked under non-billable, it is collected and computed in hours. |
| `nonBillableMinutes` | number | If the project has time entries tracked under non-billable, it is collected and computed in minutes. |
| `owner` | object | The project owner is the team member who has access to everything in the project and is in charge of managing it. Any team member can be assigned as the project owner during the project creation or can be modified later.  In the absence of a selection, the project owner is set to the team member who created the project by default. |
| `partnerCompanies` | array<object> | The `partners` field contains list of partner companies. |
| `percentageBudgetConsumed` | number | The budget consumed percentage. |
| `percentageBudgetedHoursConsumed` | number | The budgeted hours consumed percentage. |
| `plannedDurationInDays` | number | The difference between `startDate` and `dueDate` is computed and stored in days as `plannedDurationInDays`. |
| `progressPercentage` | number | The progress percentage is computed based on the number of tasks that are completed vs the total number of tasks in the project. This can be used to track how much the project has progressed over time. |
| `projectAgeInDays` | number | If both the project actual dates (`startDateActual` and `dueDateActual`) are available, the difference is computed and shown in days. If `dueDateActual` isn't available, then the value is computed by the difference of today's date and the available date under `startDateActual`. The value will be null or not present if `startDateActual` is not available. |
| `projectFee` | number | The total fee that is charged for the project. |
| `projectId` | number | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `projectName` | string | The name of the project. |
| `remainingHours` | number | Number of hours left to complete the project or task based on tracked and budgeted hours. |
| `remainingMinutes` | number | Number of minutes left to complete the project or task and complements RemainingHours. |
| `sources` | array<object> | Sources denotes the project templates involved in creation/ imported post creation of the project. |
| `startDate` | string | On this date the project's execution officially begins. If sources (templates) are mentioned in the request, the start date is required. For projects without any defined sources, it may be empty. The format for the start date is _YYYY-MM-DD_. |
| `startDateActual` | string | The date on which the project status is changed to in progress. The status can be either the default said status (in progress) or custom statuses that are categorised as in progress. It can be null for projects that have not yet begun. The format for the actual start date is _YYYY-MM-DD_. |
| `status` | object | The project status value along with the label will be present here. |
| `teamMembers` | object | The teamMembers field can be used to specify the project members, customers and customerChampion. Once the project is created, an invite will be emailed to all the teamMembers specified. |
| `trackedHours` | number | The number of hours tracked as part of `submitted` time-entries are captured here and computed in hours. |
| `trackedMinutes` | number | The number of minutes tracked as part of `submitted` time-entries are captured here and computed in minutes. |
| `updatedAt` | number | The time when the project was updated. Any changes that's related to the project are captured and specified here in epoch millis. |
| `updatedBy` | object | The team member who updated the project |
| `visibility` | string | Set visibility parameters to restrict who can see your project. There are two options: `EVERYONE` and `MEMBERS`. Selecting `EVERYONE` allows all team members from your firm to view the project, while selecting `MEMBER` restricts access to only those team members who have been specifically invited. |

## Native endpoint

Through the native Rocketlane API, this operation is `GET /1.0/projects` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

