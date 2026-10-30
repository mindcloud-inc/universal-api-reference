# <img src="https://images.mindcloud.co/apps/icons/go-canvas_1793296209949.png" alt="GoCanvas logo" width="28" height="28"> GoCanvas: Universal API

Manage users, department memberships, form assignments, and reference data in GoCanvas.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goCanvas/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 85
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gocanvas.com
- **Vendor API docs:** https://api.gocanvas.com/api/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (85)

### Available Task

| Action | Method | Description |
| --- | --- | --- |
| [List Available Tasks](actions/list-available-tasks.md) | GET |  |

### Binary Upload Status

| Action | Method | Description |
| --- | --- | --- |
| [List Binary Upload Statuses](actions/list-binary-upload-statuses.md) | GET |  |

### Cloud Save

| Action | Method | Description |
| --- | --- | --- |
| [List Cloud Saves](actions/list-cloud-saves.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Child Companies](actions/list-child-companies.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Child Company](actions/create-child-company.md) | POST |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Delete Customer](actions/delete-customer.md) | DELETE |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Retrieve Customer](actions/retrieve-customer.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST |  |
| [List Departments](actions/list-departments.md) | GET |  |
| [List Form Shared Departments](actions/list-form-shared-departments.md) | GET |  |
| [Share Form with Departments](actions/share-form-with-departments.md) | POST |  |

### Dispatch

| Action | Method | Description |
| --- | --- | --- |
| [Create Dispatch](actions/create-dispatch.md) | POST |  |
| [Delete Dispatch](actions/delete-dispatch.md) | DELETE |  |
| [List Dispatches](actions/list-dispatches.md) | GET |  |
| [Mark Dispatch as Received](actions/mark-dispatch-as-received.md) | PUT |  |
| [Retrieve Dispatch](actions/retrieve-dispatch.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form](actions/delete-form.md) | DELETE |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Retrieve Basic Form PDF](actions/retrieve-basic-form-pdf.md) | GET |  |
| [Retrieve Form](actions/retrieve-form.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Assign Form to Group](actions/assign-form-to-group.md) | POST |  |
| [Assign User to Group](actions/assign-user-to-group.md) | POST |  |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Remove Form from Group](actions/remove-form-from-group.md) | DELETE |  |
| [Remove User from Group](actions/remove-user-from-group.md) | DELETE |  |
| [Retrieve Group](actions/retrieve-group.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET |  |
| [List Tracker Locations](actions/list-tracker-locations.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Project](actions/retrieve-project.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Reference Data

| Action | Method | Description |
| --- | --- | --- |
| [Create Reference Data](actions/create-reference-data.md) | POST |  |
| [List Reference Data](actions/list-reference-data.md) | GET |  |
| [Retrieve Reference Data](actions/retrieve-reference-data.md) | GET |  |
| [Update Reference Data](actions/update-reference-data.md) | PUT |  |

### Reference Image

| Action | Method | Description |
| --- | --- | --- |
| [List Reference Images](actions/list-reference-images.md) | GET |  |
| [Retrieve Multiple Reference Images](actions/retrieve-multiple-reference-images.md) | GET |  |
| [Retrieve Reference Image](actions/retrieve-reference-image.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Submission Report PDF](actions/generate-submission-report-pdf.md) | GET |  |
| [List Form Reports](actions/list-form-reports.md) | GET |  |
| [Retrieve Form Report](actions/retrieve-form-report.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Delete Site](actions/delete-site.md) | DELETE |  |
| [Retrieve Site](actions/retrieve-site.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Submission](actions/create-submission.md) | POST |  |
| [Delete Submission](actions/delete-submission.md) | DELETE |  |
| [List Submissions](actions/list-submissions.md) | GET |  |
| [Replace Submission](actions/replace-submission.md) | PUT |  |
| [Retrieve Default Submission PDF](actions/retrieve-default-submission-pdf.md) | GET |  |
| [Retrieve Standard Submission PDF](actions/retrieve-standard-submission-pdf.md) | GET |  |
| [Retrieve Submission](actions/retrieve-submission.md) | GET |  |
| [Update Submission](actions/update-submission.md) | PUT |  |

### Submission Revision

| Action | Method | Description |
| --- | --- | --- |
| [List Submission Revisions](actions/list-submission-revisions.md) | GET |  |

### Submission Value

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission Value](actions/delete-submission-value.md) | DELETE |  |
| [Retrieve Submission Value](actions/retrieve-submission-value.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Department](actions/add-user-to-department.md) | POST |  |
| [Assign User to Form](actions/assign-user-to-form.md) | POST |  |
| [Change User Password](actions/change-user-password.md) | PUT |  |
| [Create User](actions/create-user.md) | POST |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get Current User Capabilities](actions/get-current-user-capabilities.md) | GET |  |
| [List Department Users](actions/list-department-users.md) | GET |  |
| [List Form Users](actions/list-form-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Retrieve User](actions/retrieve-user.md) | GET |  |
| [Unassign User from Form](actions/unassign-user-from-form.md) | DELETE |  |
| [Update User](actions/update-user.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET |  |
| [Test Webhook](actions/test-webhook.md) | POST |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Workflow](actions/retrieve-workflow.md) | GET |  |

### Workflow Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow History](actions/list-workflow-history.md) | GET |  |
| [List Workflow Submissions](actions/list-workflow-submissions.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET |  |

