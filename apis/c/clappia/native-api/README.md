# Clappia: Native API Reference

A consolidated summary of Clappia's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.clappia.com/
- **API base URL:** `https://api-public-v4.clappia.com`

## Authentication

### API Key

Connect Clappia with a workplace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.clappia.com/help/clappia-public-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `users`. The next-page cursor is read from `token`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Chart](actions/add-chart.md) | `POST /analytics/addChart` | [docs](https://developer.clappia.com/) |
| [Add Field](actions/add-field.md) | `POST /appdefinitionv2/addField` | [docs](https://developer.clappia.com/) |
| [Add Page Break](actions/add-page-break.md) | `POST /appdefinitionv2/addPageBreak` | [docs](https://developer.clappia.com/) |
| [Add Section](actions/add-section.md) | `POST /appdefinitionv2/addSection` | [docs](https://developer.clappia.com/) |
| [Add User to App](actions/add-user-to-app.md) | `POST /app/addUserToApp` | [docs](https://developer.clappia.com/) |
| [Add User to Workplace](actions/add-user-to-workplace.md) | `POST /workplace/addUserToWorkplace` | [docs](https://developer.clappia.com/) |
| [Add Workflow Step](actions/add-workflow-step.md) | `POST /workflowdefinitionv2/addWorkflowStep` | [docs](https://developer.clappia.com/) |
| [Create App Version](actions/create-app-version.md) | `POST /appdefinitionv2/createNewAppVersion` | [docs](https://developer.clappia.com/) |
| [Create Submission](actions/create-submission.md) | `POST /submissions/create` | [docs](https://developer.clappia.com/) |
| [Get App Definition](actions/get-app-definition.md) | `GET /appdefinitionv2/getAppDefinition` | [docs](https://developer.clappia.com/) |
| [Get App Workflow](actions/get-app-workflow.md) | `GET /workflowdefinitionv2/getWorkflow` | [docs](https://developer.clappia.com/) |
| [Get Submission](actions/get-submission.md) | `GET /submissions/getSubmission` | [docs](https://developer.clappia.com/) |
| [Get Submissions Aggregation](actions/get-submissions-aggregation.md) | `POST /submissions/getSubmissionsAggregation` | [docs](https://developer.clappia.com/) |
| [Get Submissions Count](actions/get-submissions-count.md) | `POST /submissions/getSubmissionsCount` | [docs](https://developer.clappia.com/) |
| [Get Submissions Excel](actions/get-submissions-excel.md) | `POST /submissions/getSubmissionsExcel` | [docs](https://developer.clappia.com/) |
| [List App Versions](actions/list-app-versions.md) | `GET /appdefinitionv2/getAppVersions` | [docs](https://developer.clappia.com/) |
| [List Charts](actions/list-charts.md) | `GET /analytics/getAppCharts` | [docs](https://developer.clappia.com/) |
| [List User Apps by Email](actions/list-user-apps-by-email.md) | `GET /workplace/getUserApps` | [docs](https://developer.clappia.com/) |
| [List User Apps by Phone](actions/list-user-apps-by-phone.md) | `GET /workplace/getUserApps` | [docs](https://developer.clappia.com/) |
| [List Workplace Apps](actions/list-workplace-apps.md) | `GET /workplace/getApps` | [docs](https://developer.clappia.com/) |
| [List Workplace Users](actions/list-workplace-users.md) | `POST /workplace/getWorkplaceUsers` | [docs](https://developer.clappia.com/) |
| [Reorder Chart](actions/reorder-chart.md) | `POST /analytics/reorderChart` | [docs](https://developer.clappia.com/) |
| [Reorder Field](actions/reorder-field.md) | `POST /appdefinitionv2/reorderField` | [docs](https://developer.clappia.com/) |
| [Reorder Section](actions/reorder-section.md) | `POST /appdefinitionv2/reorderSection` | [docs](https://developer.clappia.com/) |
| [Reorder Workflow Step](actions/reorder-workflow-step.md) | `POST /workflowdefinitionv2/reorderWorkflowStep` | [docs](https://developer.clappia.com/) |
| [Search Submissions](actions/search-submissions.md) | `POST /submissions/getSubmissions` | [docs](https://developer.clappia.com/) |
| [Update App Live Version](actions/update-app-live-version.md) | `POST /appdefinitionv2/updateLiveVersion` | [docs](https://developer.clappia.com/) |
| [Update App Metadata](actions/update-app-metadata.md) | `POST /appdefinitionv2/updateAppMetadata` | [docs](https://developer.clappia.com/) |
| [Update App Version](actions/update-app-version.md) | `POST /appdefinitionv2/updateAppVersion` | [docs](https://developer.clappia.com/) |
| [Update Chart](actions/update-chart.md) | `POST /analytics/updateChart` | [docs](https://developer.clappia.com/) |
| [Update Field](actions/update-field.md) | `POST /appdefinitionv2/updateField` | [docs](https://developer.clappia.com/) |
| [Update Page Break](actions/update-page-break.md) | `POST /appdefinitionv2/updatePageBreak` | [docs](https://developer.clappia.com/) |
| [Update Submission](actions/update-submission.md) | `POST /submissions/edit` | [docs](https://developer.clappia.com/) |
| [Update Submission Owners](actions/update-submission-owners.md) | `POST /submissions/updateSubmissionOwners` | [docs](https://developer.clappia.com/) |
| [Update Submission Status](actions/update-submission-status.md) | `POST /submissions/updateStatus` | [docs](https://developer.clappia.com/) |
| [Update Workflow Step](actions/update-workflow-step.md) | `POST /workflowdefinitionv2/updateWorkflowStep` | [docs](https://developer.clappia.com/) |
| [Update Workplace User Attributes](actions/update-workplace-user-attributes.md) | `POST /workplace/updateWorkplaceUserAttributes` | [docs](https://developer.clappia.com/) |
| [Update Workplace User Details](actions/update-workplace-user-details.md) | `POST /workplace/updateWorkplaceUserDetails` | [docs](https://developer.clappia.com/) |
| [Update Workplace User Groups](actions/update-workplace-user-groups.md) | `POST /workplace/updateWorkplaceUserGroups` | [docs](https://developer.clappia.com/) |
| [Update Workplace User Role](actions/update-workplace-user-role.md) | `POST /workplace/updateWorkplaceUserRole` | [docs](https://developer.clappia.com/) |
