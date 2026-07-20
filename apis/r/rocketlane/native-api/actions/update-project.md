# Update Project with Rocketlane

Updates a project in Rocketlane.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.0/projects/:projectId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Update Project](https://developer.rocketlane.com/reference/update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `projectName` | body | `string` | no | The `name` of the project. The name specified will be displayed everywhere else and can be used for filtering purposes. |
| `startDate` | body | `string` | no | On this date the project's execution officially begins. If sources (templates) are mentioned in the request, the start date is required. For projects without any defined sources, it may be empty. The format for the start date is _YYYY-MM-DD_. |
| `dueDate` | body | `string` | no | The day on which the project's execution is planned to be completed. The due date is not required and can be left blank. If sources (templates) are included as part of the project creation, the project's due date will be calculated depending on the duration of the specified sources. For projects where both `startDate` and `dueDate` are specified, the latter must be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `visibility` | body | `string` | no | Set visibility parameters to restrict who can see your project. There are two options: `EVERYONE` and `MEMBERS`. Selecting `EVERYONE` allows all team members from your firm to view the project, while selecting `MEMBERS` restricts access to only those team members who have been specifically invited. |
| `owner` | body | `object` | no | The project owner gets access to everything in the project and can be used to control the activities that happens in the project. Note: Changing the owner can result in `transfer of ownership` from the older member to the specified member. All the access for the older member will be `revoked`. |
| `status` | body | `object` | no | The value of the project status can be specified here and this is essential to keep track of the project. |
| `fields` | body | `list<object>` | no | The custom fields can be set during the project creation with the help of `fields`. The `fieldValue` can be either a string or a number or an array and it has to comply with the type of the field. Refer [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know how to assign `fieldValue` based on their `field_type`. |
| `annualizedRecurringRevenue` | body | `number` | no | Indicates the value of the recurring revenue of the customer's subscriptions for a single calendar year. |
| `projectFee` | body | `number` | no | The total fee that is charged for the project. |
| `autoAllocation` | body | `boolean` | no | The field autoAllocation defines whether Auto Allocation is enabled for the project or not. If auto allocation is enabled, instead of adding it manually, the allocations are computed from the tasks duration, effort and the assignees specified in the project. |
| `budgetedHours` | body | `number` | no | Budgeted hours represent the total hours allocated for project execution. This value can be edited at any point throughout the project's duration. You can enter the budgeted hours in decimal form, including both hours and minutes, with up to two decimal places of precision. Eg: 1.65 hrs = 1h 39m(1.65h * 60m = 99m). |
| `externalReferenceId` | body | `string` | no | An externalReferenceId is a unique identifier that links entities or transactions between external systems and Rocketlane, ensuring accurate data correlation and consistency. |
