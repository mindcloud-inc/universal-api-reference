# <img src="https://images.mindcloud.co/apps/icons/clappia_1774981917205.png" alt="Clappia logo" width="28" height="28"> Clappia: Universal API

Create forms, workflows, dashboards, and business apps with Clappia

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clappia/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clappia.com
- **Vendor API docs:** https://developer.clappia.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workplace Users](actions/list-workplace-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Get App Definition](actions/get-app-definition.md) | GET | Retrieves app definition details from Clappia. |
| [List User Apps by Email](actions/list-user-apps-by-email.md) | GET | Retrieves user apps from Clappia by email address. |
| [List User Apps by Phone](actions/list-user-apps-by-phone.md) | GET | Retrieves user apps from Clappia by phone number. |
| [List Workplace Apps](actions/list-workplace-apps.md) | GET | Retrieves workplace app records from Clappia. |
| [Update App Metadata](actions/update-app-metadata.md) | PUT | Updates existing app metadata in Clappia. |

### App Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Field](actions/add-field.md) | POST | Creates a new app field in Clappia. |
| [Reorder Field](actions/reorder-field.md) | PUT | Updates app field order in Clappia. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing app field in Clappia. |

### App Section

| Action | Method | Description |
| --- | --- | --- |
| [Add Section](actions/add-section.md) | POST | Creates a new app section in Clappia. |
| [Reorder Section](actions/reorder-section.md) | PUT | Updates app section order in Clappia. |

### App User

| Action | Method | Description |
| --- | --- | --- |
| [Add User to App](actions/add-user-to-app.md) | POST | Creates a new app user membership in Clappia. |

### App Version

| Action | Method | Description |
| --- | --- | --- |
| [Create App Version](actions/create-app-version.md) | POST | Creates a new app version in Clappia. |
| [List App Versions](actions/list-app-versions.md) | GET | Retrieves app version records from Clappia. |
| [Update App Live Version](actions/update-app-live-version.md) | PUT | Updates the live app version in Clappia. |
| [Update App Version](actions/update-app-version.md) | PUT | Updates an existing app version in Clappia. |

### Chart

| Action | Method | Description |
| --- | --- | --- |
| [Add Chart](actions/add-chart.md) | POST | Creates a new chart in Clappia. |
| [List Charts](actions/list-charts.md) | GET | Retrieves app chart records from Clappia. |
| [Reorder Chart](actions/reorder-chart.md) | PUT | Updates chart display order in Clappia. |
| [Update Chart](actions/update-chart.md) | PUT | Updates an existing chart in Clappia. |

### Page Break

| Action | Method | Description |
| --- | --- | --- |
| [Add Page Break](actions/add-page-break.md) | POST | Creates a new page break in Clappia. |
| [Update Page Break](actions/update-page-break.md) | PUT | Updates an existing page break in Clappia. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Submission](actions/create-submission.md) | POST | Creates a new submission in Clappia. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a submission record from Clappia. |
| [Search Submissions](actions/search-submissions.md) | GET | Finds submissions in Clappia by search criteria. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in Clappia. |
| [Update Submission Owners](actions/update-submission-owners.md) | PUT | Updates submission owners for an existing Clappia submission. |
| [Update Submission Status](actions/update-submission-status.md) | PUT | Updates an existing submission status in Clappia. |

### Submission Aggregation

| Action | Method | Description |
| --- | --- | --- |
| [Get Submissions Aggregation](actions/get-submissions-aggregation.md) | GET | Retrieves submission aggregation results from Clappia. |

### Submission Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Submissions Count](actions/get-submissions-count.md) | GET | Retrieves the matching submissions count from Clappia. |

### Submission Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Submissions Excel](actions/get-submissions-excel.md) | GET | Retrieves a submissions export file from Clappia. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get App Workflow](actions/get-app-workflow.md) | GET | Retrieves app workflow details from Clappia. |

### Workflow Step

| Action | Method | Description |
| --- | --- | --- |
| [Add Workflow Step](actions/add-workflow-step.md) | POST | Creates a new workflow step in Clappia. |
| [Reorder Workflow Step](actions/reorder-workflow-step.md) | PUT | Updates workflow step order in Clappia. |
| [Update Workflow Step](actions/update-workflow-step.md) | PUT | Updates an existing workflow step in Clappia. |

### Workplace User

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Workplace](actions/add-user-to-workplace.md) | POST | Creates a new workplace user in Clappia. |
| [List Workplace Users](actions/list-workplace-users.md) | GET | Retrieves workplace users from your Clappia workplace. |
| [Update Workplace User Attributes](actions/update-workplace-user-attributes.md) | PUT | Updates workplace user attributes in Clappia. |
| [Update Workplace User Details](actions/update-workplace-user-details.md) | PUT | Updates workplace user details in Clappia. |
| [Update Workplace User Groups](actions/update-workplace-user-groups.md) | PUT | Updates workplace user groups in Clappia. |
| [Update Workplace User Role](actions/update-workplace-user-role.md) | PUT | Updates workplace user role assignments in Clappia. |

