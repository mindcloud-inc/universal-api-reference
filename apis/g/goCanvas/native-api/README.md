# GoCanvas: Native API Reference

A consolidated summary of GoCanvas's API configuration and 85 documented operations, with links to official documentation.

- **Official docs:** https://api.gocanvas.com/api/v3/docs
- **API base URL:** `https://www.gocanvas.com/api/v3`

## Authentication

### Basic Auth

Connect using your GoCanvas username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.gocanvas.com/api/v3/docs#authentication-basic)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (85 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User to Department](actions/add-user-to-department.md) | `POST /departments/:departmentId/users` | [docs](https://api.gocanvas.com/api/v3/docs#add-a-user-to-a-department) |
| [Assign Form to Group](actions/assign-form-to-group.md) | `POST /groups/:groupId/forms` | [docs](https://api.gocanvas.com/api/v3/docs#assign-form-to-group) |
| [Assign User to Form](actions/assign-user-to-form.md) | `POST /forms/:formId/assigned_users` | [docs](https://api.gocanvas.com/api/v3/docs#assign-user-to-form) |
| [Assign User to Group](actions/assign-user-to-group.md) | `POST /groups/:groupId/users` | [docs](https://api.gocanvas.com/api/v3/docs#assign-user-to-group) |
| [Change User Password](actions/change-user-password.md) | `PATCH /users/:userId/change_password` | [docs](https://api.gocanvas.com/api/v3/docs#change-user-password) |
| [Create Child Company](actions/create-child-company.md) | `POST /companies` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-child-company) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-customer) |
| [Create Department](actions/create-department.md) | `POST /departments` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-department) |
| [Create Dispatch](actions/create-dispatch.md) | `POST /dispatches` | [docs](https://api.gocanvas.com/api/v3/docs#create-an-immediate-dispatch) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-group) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-project) |
| [Create Reference Data](actions/create-reference-data.md) | `POST /reference_data` | [docs](https://api.gocanvas.com/api/v3/docs#create-reference-data) |
| [Create Site](actions/create-site.md) | `POST /sites` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-site) |
| [Create Submission](actions/create-submission.md) | `POST /submissions` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-basic-submission) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-user) |
| [Create Webhook](actions/create-webhook.md) | `POST /forms/:formId/webhooks` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-webhook) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:customerId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-customer) |
| [Delete Dispatch](actions/delete-dispatch.md) | `DELETE /dispatches/:dispatchId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-dispatch) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms/:formId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-form) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:groupId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-group) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:projectId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-project) |
| [Delete Site](actions/delete-site.md) | `DELETE /sites/:siteId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-site) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /submissions/:submissionId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-submission) |
| [Delete Submission Value](actions/delete-submission-value.md) | `DELETE /submissions/:submissionId/values/:valueId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-value) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /forms/:formId/webhooks/:webhookId` | [docs](https://api.gocanvas.com/api/v3/docs#delete-a-webhook) |
| [Generate Submission Report PDF](actions/generate-submission-report-pdf.md) | `GET /submissions/:submissionId/reports/:reportId` | [docs](https://api.gocanvas.com/api/v3/docs#generate-pdf-with-report-id) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://api.gocanvas.com/api/v3/docs#current-user-profile) |
| [Get Current User Capabilities](actions/get-current-user-capabilities.md) | `GET /me/capabilities` | [docs](https://api.gocanvas.com/api/v3/docs#current-user-capabilities) |
| [List Available Tasks](actions/list-available-tasks.md) | `GET /workflows/available_tasks` | [docs](https://api.gocanvas.com/api/v3/docs#list-available-tasks) |
| [List Binary Upload Statuses](actions/list-binary-upload-statuses.md) | `GET /submissions/:submissionId/values` | [docs](https://api.gocanvas.com/api/v3/docs#list-binary-upload-statuses) |
| [List Child Companies](actions/list-child-companies.md) | `GET /partnership/companies` | [docs](https://api.gocanvas.com/api/v3/docs#list-child-companies) |
| [List Cloud Saves](actions/list-cloud-saves.md) | `GET /submissions/cloud_saves` | [docs](https://api.gocanvas.com/api/v3/docs#list-cloud-saves) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-customers) |
| [List Department Users](actions/list-department-users.md) | `GET /departments/:departmentId/users` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-department-users) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-departments) |
| [List Dispatches](actions/list-dispatches.md) | `GET /dispatches` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-dispatches) |
| [List Form Reports](actions/list-form-reports.md) | `GET /forms/:formId/reports` | [docs](https://api.gocanvas.com/api/v3/docs#list-of-reports-by-form) |
| [List Form Shared Departments](actions/list-form-shared-departments.md) | `GET /forms/:formId/shared_departments` | [docs](https://api.gocanvas.com/api/v3/docs#shared-departments-for-form) |
| [List Form Users](actions/list-form-users.md) | `GET /forms/:formId/assigned_users` | [docs](https://api.gocanvas.com/api/v3/docs#assigned-users-for-form) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-forms) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-groups) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-projects) |
| [List Reference Data](actions/list-reference-data.md) | `GET /reference_data` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-reference-data) |
| [List Reference Images](actions/list-reference-images.md) | `GET /reference_images` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-reference-images) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-sites) |
| [List Submission Revisions](actions/list-submission-revisions.md) | `GET /submissions/:submissionId/revisions` | [docs](https://api.gocanvas.com/api/v3/docs#list-of-revisions-by-submission) |
| [List Submissions](actions/list-submissions.md) | `GET /submissions` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-submissions) |
| [List Tracker Locations](actions/list-tracker-locations.md) | `GET /tracker/locations` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-locations) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /forms/:formId/webhooks` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-webhooks) |
| [List Workflow History](actions/list-workflow-history.md) | `GET /workflows/history` | [docs](https://api.gocanvas.com/api/v3/docs#workflow-history) |
| [List Workflow Submissions](actions/list-workflow-submissions.md) | `GET /workflows/submissions` | [docs](https://api.gocanvas.com/api/v3/docs#list-workflow-submissions) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://api.gocanvas.com/api/v3/docs#workflow-summary) |
| [Mark Dispatch as Received](actions/mark-dispatch-as-received.md) | `PATCH /dispatches/:dispatchId` | [docs](https://api.gocanvas.com/api/v3/docs#mark-a-dispatch-as-received) |
| [Remove Form from Group](actions/remove-form-from-group.md) | `DELETE /groups/:groupId/forms/:formId` | [docs](https://api.gocanvas.com/api/v3/docs#remove-form-from-group) |
| [Remove User from Group](actions/remove-user-from-group.md) | `DELETE /groups/:groupId/users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#remove-user-from-group) |
| [Replace Submission](actions/replace-submission.md) | `PUT /submissions/:submissionId` | [docs](https://api.gocanvas.com/api/v3/docs#replace-a-submission) |
| [Retrieve Basic Form PDF](actions/retrieve-basic-form-pdf.md) | `GET /forms/:formId/basic_pdf` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-basic-form-pdf) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:customerId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-customer) |
| [Retrieve Default Submission PDF](actions/retrieve-default-submission-pdf.md) | `GET /submissions/:submissionId/pdf` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-the-default-report) |
| [Retrieve Dispatch](actions/retrieve-dispatch.md) | `GET /dispatches/:dispatchId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-dispatch) |
| [Retrieve Form](actions/retrieve-form.md) | `GET /forms/:formId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-form) |
| [Retrieve Form Report](actions/retrieve-form-report.md) | `GET /forms/:formId/reports/:reportId` | [docs](https://api.gocanvas.com/api/v3/docs#single-report-by-form) |
| [Retrieve Group](actions/retrieve-group.md) | `GET /groups/:groupId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-group) |
| [Retrieve Multiple Reference Images](actions/retrieve-multiple-reference-images.md) | `GET /reference_images/bulk` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-multiple-reference-images) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/:projectId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-project) |
| [Retrieve Reference Data](actions/retrieve-reference-data.md) | `GET /reference_data/:referenceDataId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-reference-data) |
| [Retrieve Reference Image](actions/retrieve-reference-image.md) | `GET /reference_images/:referenceImageId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-reference-image) |
| [Retrieve Site](actions/retrieve-site.md) | `GET /sites/:siteId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-site) |
| [Retrieve Standard Submission PDF](actions/retrieve-standard-submission-pdf.md) | `GET /submissions/:submissionId/standard_pdf` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-the-standard-report) |
| [Retrieve Submission](actions/retrieve-submission.md) | `GET /submissions/:submissionId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-submission) |
| [Retrieve Submission Value](actions/retrieve-submission-value.md) | `GET /submissions/:submissionId/values/:valueId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-value) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-user) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /forms/:formId/webhooks/:webhookId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-webhook) |
| [Retrieve Workflow](actions/retrieve-workflow.md) | `GET /workflows/:workflowId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-workflow) |
| [Share Form with Departments](actions/share-form-with-departments.md) | `POST /forms/:formId/shared_departments` | [docs](https://api.gocanvas.com/api/v3/docs#share-form-with-departments) |
| [Test Webhook](actions/test-webhook.md) | `POST /forms/:formId/webhooks/:webhookId/test` | [docs](https://api.gocanvas.com/api/v3/docs#test-a-webhook) |
| [Unassign User from Form](actions/unassign-user-from-form.md) | `DELETE /forms/:formId/assigned_users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#unassign-user-from-form) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/:customerId` | [docs](https://api.gocanvas.com/api/v3/docs#update-a-customer) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:projectId` | [docs](https://api.gocanvas.com/api/v3/docs#update-a-project) |
| [Update Reference Data](actions/update-reference-data.md) | `PATCH /reference_data/:referenceDataId` | [docs](https://api.gocanvas.com/api/v3/docs#update-reference-data) |
| [Update Site](actions/update-site.md) | `PATCH /sites/:siteId` | [docs](https://api.gocanvas.com/api/v3/docs#update-a-site) |
| [Update Submission](actions/update-submission.md) | `PATCH /submissions/:submissionId` | [docs](https://api.gocanvas.com/api/v3/docs#update-a-submission) |
| [Update User](actions/update-user.md) | `PATCH /users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#update-user) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /forms/:formId/webhooks/:webhookId` | [docs](https://api.gocanvas.com/api/v3/docs#update-a-webhook) |
