# Clockify: Native API Reference

A consolidated summary of Clockify's API configuration and 154 documented operations, with links to official documentation.

- **Official docs:** https://docs.developer.clockify.me/
- **OpenAPI specification:** https://docs.developer.clockify.me/openapi.json
- **API base URL:** `https://api.clockify.me/api/v1`

## Authentication

### API Key

Clockify personal API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://clockify.me/help/getting-started/manage-your-profile-settings)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page-size` in the query string to set the page size (default 50; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort-column` in the query string. Set the direction separately with `sort-order`. Use `ASCENDING` for ascending order and `DESCENDING` for descending order. Only one sort field is accepted.

## Endpoints (154 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Manager Role to User](actions/add-manager-role-to-user.md) | `POST workspaces/:workspaceId/users/:userId/roles` | [docs](https://docs.developer.clockify.me/#tag/User/operation/createUserRole) |
| [Add User to Workspace](actions/add-user-to-workspace.md) | `POST workspaces/:workspaceId/users` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/addUsers) |
| [Add Users to Group](actions/add-users-to-group.md) | `POST workspaces/:workspaceId/user-groups/:userGroupId/users` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/addUser) |
| [Add Users to Project](actions/add-users-to-project.md) | `POST workspaces/:workspaceId/projects/:projectId/memberships` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/addUsersToProject) |
| [Archive Expense Category](actions/archive-expense-category.md) | `PATCH workspaces/:workspaceId/expenses/categories/:categoryId/status` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/updateExpenseCategoryStatus) |
| [Change Invoice Status](actions/change-invoice-status.md) | `PATCH workspaces/:workspaceId/invoices/:invoiceId/status` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/changeInvoiceStatus) |
| [Change Policy Status](actions/change-policy-status.md) | `PATCH workspaces/:workspaceId/time-off/policies/:id` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/updatePolicyStatus) |
| [Change Recurring Period](actions/change-recurring-period.md) | `PUT workspaces/:workspaceId/scheduling/assignments/series/:assignmentId` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/editRecurringPeriod) |
| [Change Time Off Request Status](actions/change-time-off-request-status.md) | `PATCH workspaces/:workspaceId/time-off/policies/:policyId/requests/:requestId` | [docs](https://docs.developer.clockify.me/#tag/Time-Off/operation/changeTimeOffRequestStatus) |
| [Copy Scheduled Assignment](actions/copy-scheduled-assignment.md) | `POST workspaces/:workspaceId/scheduling/assignments/:assignmentId/copy` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/copyAssignment) |
| [Create Expense](actions/create-expense.md) | `POST workspaces/:workspaceId/expenses` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/createExpense) |
| [Create Expense Category](actions/create-expense-category.md) | `POST workspaces/:workspaceId/expenses/categories` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/createExpenseCategory) |
| [Create Group](actions/create-group.md) | `POST workspaces/:workspaceId/user-groups` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/createUserGroup) |
| [Create Holiday](actions/create-holiday.md) | `POST workspaces/:workspaceId/holidays` | [docs](https://docs.developer.clockify.me/#tag/Holiday/operation/createHoliday) |
| [Create Invoice](actions/create-invoice.md) | `POST workspaces/:workspaceId/invoices` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/createInvoice) |
| [Create Invoice Payment](actions/create-invoice-payment.md) | `POST workspaces/:workspaceId/invoices/:invoiceId/payments` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/createInvoicePayment) |
| [Create Project](actions/create-project.md) | `POST workspaces/:workspaceId/projects` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/createNewProject) |
| [Create Project Task](actions/create-project-task.md) | `POST workspaces/:workspaceId/projects/:projectId/tasks` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/createTask) |
| [Create Recurring Assignment](actions/create-recurring-assignment.md) | `POST workspaces/:workspaceId/scheduling/assignments/recurring` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/createRecurring) |
| [Create Shared Report](actions/create-shared-report.md) | `POST workspaces/:workspaceId/shared-reports` | [docs](https://docs.developer.clockify.me/#tag/Shared-Report/operation/saveSharedReportV1) |
| [Create Time Entry](actions/create-time-entry.md) | `POST workspaces/:workspaceId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/createTimeEntry) |
| [Create Time Off Policy](actions/create-time-off-policy.md) | `POST workspaces/:workspaceId/time-off/policies` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/createPolicy) |
| [Create Time Off Request](actions/create-time-off-request.md) | `POST workspaces/:workspaceId/time-off/policies/:policyId/requests` | [docs](https://docs.developer.clockify.me/#tag/Time-Off/operation/createTimeOffRequest) |
| [Create User Time Entry](actions/create-user-time-entry.md) | `POST workspaces/:workspaceId/user/:userId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/createForOthers) |
| [Create User Time Off Request](actions/create-user-time-off-request.md) | `POST workspaces/:workspaceId/time-off/policies/:policyId/users/:userId/requests` | [docs](https://docs.developer.clockify.me/#tag/Time-Off/operation/createTimeOffRequestForOther) |
| [Create Webhook](actions/create-webhook.md) | `POST workspaces/:workspaceId/webhooks` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/createWebhook) |
| [Create Workspace](actions/create-workspace.md) | `POST workspaces` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/createWorkspace) |
| [Create Workspace Client](actions/create-workspace-client.md) | `POST workspaces/:workspaceId/clients` | [docs](https://docs.developer.clockify.me/#tag/Client/operation/createClient) |
| [Create Workspace Custom Field](actions/create-workspace-custom-field.md) | `POST workspaces/:workspaceId/custom-fields` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/create) |
| [Create Workspace Tag](actions/create-workspace-tag.md) | `POST workspaces/:workspaceId/tags` | [docs](https://docs.developer.clockify.me/#tag/Tag/operation/createNewTag) |
| [Delete Client](actions/delete-client.md) | `DELETE workspaces/:workspaceId/clients/:id` | [docs](https://docs.developer.clockify.me/#tag/Client/operation/deleteClient) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE workspaces/:workspaceId/custom-fields/:customFieldId` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/delete) |
| [Delete Expense](actions/delete-expense.md) | `DELETE workspaces/:workspaceId/expenses/:expenseId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/deleteExpense) |
| [Delete Expense Category](actions/delete-expense-category.md) | `DELETE workspaces/:workspaceId/expenses/categories/:categoryId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/deleteCategory) |
| [Delete Group](actions/delete-group.md) | `DELETE workspaces/:workspaceId/user-groups/:id` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/deleteUserGroup) |
| [Delete Holiday](actions/delete-holiday.md) | `DELETE workspaces/:workspaceId/holidays/:holidayId` | [docs](https://docs.developer.clockify.me/#tag/Holiday/operation/deleteHoliday) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE workspaces/:workspaceId/invoices/:invoiceId` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/deleteInvoice) |
| [Delete Invoice Payment](actions/delete-invoice-payment.md) | `DELETE workspaces/:workspaceId/invoices/:invoiceId/payments/:paymentId` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/deletePaymentById) |
| [Delete Policy](actions/delete-policy.md) | `DELETE workspaces/:workspaceId/time-off/policies/:id` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/deletePolicy) |
| [Delete Project](actions/delete-project.md) | `DELETE workspaces/:workspaceId/projects/:projectId` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/deleteProject) |
| [Delete Project Task](actions/delete-project-task.md) | `DELETE workspaces/:workspaceId/projects/:projectId/tasks/:taskId` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/deleteTask) |
| [Delete Recurring Assignment](actions/delete-recurring-assignment.md) | `DELETE workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/deleteRRecurringAssignment) |
| [Delete Shared Report](actions/delete-shared-report.md) | `DELETE workspaces/:workspaceId/shared-reports/:id` | [docs](https://docs.developer.clockify.me/#tag/Shared-Report/operation/deleteSharedReportV1) |
| [Delete Tag](actions/delete-tag.md) | `DELETE workspaces/:workspaceId/tags/:id` | [docs](https://docs.developer.clockify.me/#tag/Tag/operation/deleteTag) |
| [Delete Time Off Request](actions/delete-time-off-request.md) | `DELETE workspaces/:workspaceId/time-off/policies/:policyId/requests/:requestId` | [docs](https://docs.developer.clockify.me/#tag/Time-Off/operation/deleteTimeOffRequest) |
| [Delete User Time Entries](actions/delete-user-time-entries.md) | `DELETE workspaces/:workspaceId/user/:userId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/deleteMany) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE workspaces/:workspaceId/webhooks/:webhookId` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/deleteWebhook) |
| [Delete Workspace Time Entry](actions/delete-workspace-time-entry.md) | `DELETE workspaces/:workspaceId/time-entries/:id` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/deleteTimeEntry) |
| [Download Receipt](actions/download-receipt.md) | `GET workspaces/:workspaceId/expenses/:expenseId/files/:fileId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/downloadFile) |
| [Duplicate Invoice](actions/duplicate-invoice.md) | `POST workspaces/:workspaceId/invoices/:invoiceId/duplicate` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/duplicateInvoice) |
| [Duplicate Time Entry](actions/duplicate-time-entry.md) | `POST workspaces/:workspaceId/user/:userId/time-entries/:id/duplicate` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/duplicateTimeEntry) |
| [Export Invoice](actions/export-invoice.md) | `GET workspaces/:workspaceId/invoices/:invoiceId/export` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/exportInvoice) |
| [Generate Attendance Report](actions/generate-attendance-report.md) | `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/attendance` | [docs](https://docs.developer.clockify.me/#tag/Team-Report/operation/generateAttendanceReport) |
| [Generate Detailed Report](actions/generate-detailed-report.md) | `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/detailed` | [docs](https://docs.developer.clockify.me/#tag/Time-Entry-Report/operation/generateDetailedReport) |
| [Generate Expense Report](actions/generate-expense-report.md) | `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/expenses/detailed` | [docs](https://docs.developer.clockify.me/#tag/Expense-Report/operation/generateDetailedReportV1) |
| [Generate Shared Report](actions/generate-shared-report.md) | `GET shared-reports/:id` | [docs](https://docs.developer.clockify.me/#tag/Shared-Report/operation/generateSharedReportV1) |
| [Generate Summary Report](actions/generate-summary-report.md) | `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/summary` | [docs](https://docs.developer.clockify.me/#tag/Time-Entry-Report/operation/generateSummaryReport) |
| [Generate Webhook Token](actions/generate-webhook-token.md) | `PATCH workspaces/:workspaceId/webhooks/:webhookId/token` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/generateNewToken) |
| [Generate Weekly Report](actions/generate-weekly-report.md) | `POST https://reports.api.clockify.me/v1/workspaces/:workspaceId/reports/weekly` | [docs](https://docs.developer.clockify.me/#tag/Time-Entry-Report/operation/generateWeeklyReport) |
| [Get Client](actions/get-client.md) | `GET workspaces/:workspaceId/clients/:id` | [docs](https://docs.developer.clockify.me/#tag/Client/operation/getClient) |
| [Get Current User](actions/get-current-user.md) | `GET user` | [docs](https://docs.developer.clockify.me/#tag/User/operation/getLoggedUser) |
| [Get Expense](actions/get-expense.md) | `GET workspaces/:workspaceId/expenses/:expenseId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/getExpense) |
| [Get Filtered Project Totals](actions/get-filtered-project-totals.md) | `POST workspaces/:workspaceId/scheduling/assignments/projects/totals` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/getFilteredProjectTotals) |
| [Get Invoice](actions/get-invoice.md) | `GET workspaces/:workspaceId/invoices/:invoiceId` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoice) |
| [Get Invoice Settings](actions/get-invoice-settings.md) | `GET workspaces/:workspaceId/invoices/settings` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoiceSettings) |
| [Get Member Profile](actions/get-member-profile.md) | `GET workspaces/:workspaceId/member-profile/:userId` | [docs](https://docs.developer.clockify.me/#tag/User/operation/getMemberProfile) |
| [Get Policy Balances](actions/get-policy-balances.md) | `GET workspaces/:workspaceId/time-off/balance/policy/:policyId` | [docs](https://docs.developer.clockify.me/#tag/Balance/operation/getBalancesForPolicy) |
| [Get Project Task](actions/get-project-task.md) | `GET workspaces/:workspaceId/projects/:projectId/tasks/:taskId` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/getTask) |
| [Get Project Totals](actions/get-project-totals.md) | `GET workspaces/:workspaceId/scheduling/assignments/projects/totals/:projectId` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/getProjectTotalsForSingleProject) |
| [Get Tag](actions/get-tag.md) | `GET workspaces/:workspaceId/tags/:id` | [docs](https://docs.developer.clockify.me/#tag/Tag/operation/getTag) |
| [Get Time Off Policy](actions/get-time-off-policy.md) | `GET workspaces/:workspaceId/time-off/policies/:id` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/getPolicy) |
| [Get User Balance](actions/get-user-balance.md) | `GET workspaces/:workspaceId/time-off/balance/user/:userId` | [docs](https://docs.developer.clockify.me/#tag/Balance/operation/getBalancesForUser) |
| [Get Webhook](actions/get-webhook.md) | `GET workspaces/:workspaceId/webhooks/:webhookId` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/getWebhook) |
| [Get Webhook Logs](actions/get-webhook-logs.md) | `POST workspaces/:workspaceId/webhooks/:webhookId/logs` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/getLogsForWebhook) |
| [Get Workspace](actions/get-workspace.md) | `GET workspaces/:workspaceId` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/getWorkspaceOfUser) |
| [Get Workspace Project](actions/get-workspace-project.md) | `GET workspaces/:workspaceId/projects/:projectId` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/getProject) |
| [Get Workspace Time Entry](actions/get-workspace-time-entry.md) | `GET workspaces/:workspaceId/time-entries/:id` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/getTimeEntry) |
| [Get Workspace User Capacity Total](actions/get-workspace-user-capacity-total.md) | `GET workspaces/:workspaceId/scheduling/assignments/users/:userId/totals` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/getUserTotalsForSingleUser) |
| [Get Workspace User Capacity Totals](actions/get-workspace-user-capacity-totals.md) | `POST workspaces/:workspaceId/scheduling/assignments/user-filter/totals` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/getUserTotals) |
| [List Addon Webhooks](actions/list-addon-webhooks.md) | `GET workspaces/:workspaceId/addons/:addonId/webhooks` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/getAddonWebhooks) |
| [List Approval Requests](actions/list-approval-requests.md) | `GET workspaces/:workspaceId/approval-requests` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/getApprovalRequests) |
| [List Assignments](actions/list-assignments.md) | `GET workspaces/:workspaceId/scheduling/assignments/all` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/getAllAssignments) |
| [List Created Entities (Experimental)](actions/list-created-entities-experimental.md) | `GET workspaces/:workspaceId/entities/created` | [docs](https://docs.developer.clockify.me/#tag/Entity-changes-(Experimental)/operation/getCreatedEntityInfo) |
| [List Deleted Entities (Experimental)](actions/list-deleted-entities-experimental.md) | `GET workspaces/:workspaceId/entities/deleted` | [docs](https://docs.developer.clockify.me/#tag/Entity-changes-(Experimental)/operation/getDeletedEntityInfo) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET workspaces/:workspaceId/expenses/categories` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/getCategories) |
| [List Holidays in Period](actions/list-holidays-in-period.md) | `GET workspaces/:workspaceId/holidays/in-period` | [docs](https://docs.developer.clockify.me/#tag/Holiday/operation/getHolidaysInPeriod) |
| [List In-Progress Time Entries](actions/list-in-progress-time-entries.md) | `GET workspaces/:workspaceId/time-entries/status/in-progress` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/getInProgressTimeEntries) |
| [List Invoice Payments](actions/list-invoice-payments.md) | `GET workspaces/:workspaceId/invoices/:invoiceId/payments` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/getPaymentsForInvoice) |
| [List My Shared Reports](actions/list-my-shared-reports.md) | `GET workspaces/:workspaceId/shared-reports` | [docs](https://docs.developer.clockify.me/#tag/Shared-Report/operation/getSharedReportsV1) |
| [List Project Custom Fields](actions/list-project-custom-fields.md) | `GET workspaces/:workspaceId/projects/:projectId/custom-fields` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/getCustomFieldsOfProject) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET workspaces/:workspaceId/projects/:projectId/tasks` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/getTasks) |
| [List Updated Entities (Experimental)](actions/list-updated-entities-experimental.md) | `GET workspaces/:workspaceId/entities/updated` | [docs](https://docs.developer.clockify.me/#tag/Entity-changes-(Experimental)/operation/getUpdatedEntityInfo) |
| [List User Groups](actions/list-user-groups.md) | `GET workspaces/:workspaceId/user-groups` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/getUserGroups) |
| [List User Managers](actions/list-user-managers.md) | `GET workspaces/:workspaceId/users/:userId/managers` | [docs](https://docs.developer.clockify.me/#tag/User/operation/getManagersOfUser) |
| [List User Time Entries](actions/list-user-time-entries.md) | `GET workspaces/:workspaceId/user/:userId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/getTimeEntries) |
| [List Workspace Clients](actions/list-workspace-clients.md) | `GET workspaces/:workspaceId/clients` | [docs](https://docs.developer.clockify.me/#tag/Client/operation/getClients) |
| [List Workspace Custom Fields](actions/list-workspace-custom-fields.md) | `GET workspaces/:workspaceId/custom-fields` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/ofWorkspace) |
| [List Workspace Expenses](actions/list-workspace-expenses.md) | `GET workspaces/:workspaceId/expenses` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/getExpenses) |
| [List Workspace Holidays](actions/list-workspace-holidays.md) | `GET workspaces/:workspaceId/holidays` | [docs](https://docs.developer.clockify.me/#tag/Holiday/operation/getHolidays) |
| [List Workspace Invoices](actions/list-workspace-invoices.md) | `GET workspaces/:workspaceId/invoices` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoices) |
| [List Workspace Policies](actions/list-workspace-policies.md) | `GET workspaces/:workspaceId/time-off/policies` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/findPoliciesForWorkspace) |
| [List Workspace Projects](actions/list-workspace-projects.md) | `GET workspaces/:workspaceId/projects` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/getProjects) |
| [List Workspace Tags](actions/list-workspace-tags.md) | `GET workspaces/:workspaceId/tags` | [docs](https://docs.developer.clockify.me/#tag/Tag/operation/getTags) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET workspaces/:workspaceId/users` | [docs](https://docs.developer.clockify.me/#tag/User/operation/getUsersOfWorkspace) |
| [List Workspace Webhooks](actions/list-workspace-webhooks.md) | `GET workspaces/:workspaceId/webhooks` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/getWebhooks) |
| [List Workspaces](actions/list-workspaces.md) | `GET workspaces` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/getWorkspacesOfUser) |
| [Mark Time Entries as Invoiced](actions/mark-time-entries-as-invoiced.md) | `PATCH workspaces/:workspaceId/time-entries/invoiced` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/updateInvoicedStatus) |
| [Publish Assignments](actions/publish-assignments.md) | `PUT workspaces/:workspaceId/scheduling/assignments/publish` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/publishAssignments) |
| [Remove Manager Role from User](actions/remove-manager-role-from-user.md) | `DELETE workspaces/:workspaceId/users/:userId/roles` | [docs](https://docs.developer.clockify.me/#tag/User/operation/deleteUserRole) |
| [Remove Project Custom Field](actions/remove-project-custom-field.md) | `DELETE workspaces/:workspaceId/projects/:projectId/custom-fields/:customFieldId` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/removeDefaultValueOfProject) |
| [Remove User from Group](actions/remove-user-from-group.md) | `DELETE workspaces/:workspaceId/user-groups/:userGroupId/users/:userId` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/deleteUser) |
| [Replace Time Entries](actions/replace-time-entries.md) | `PUT workspaces/:workspaceId/user/:userId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/replaceMany) |
| [Resubmit Entries and Expenses for Approval](actions/resubmit-entries-and-expenses-for-approval.md) | `POST workspaces/:workspaceId/approval-requests/resubmit-entries-for-approval` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/resubmitApprovalRequest) |
| [Resubmit User Entries and Expenses for Approval](actions/resubmit-user-entries-and-expenses-for-approval.md) | `POST workspaces/:workspaceId/approval-requests/users/:userId/resubmit-entries-for-approval` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/resubmitApprovalRequestForOther) |
| [Search Invoices](actions/search-invoices.md) | `POST workspaces/:workspaceId/invoices/info` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoicesInfo) |
| [Search Workspace Time Off Requests](actions/search-workspace-time-off-requests.md) | `POST workspaces/:workspaceId/time-off/requests` | [docs](https://docs.developer.clockify.me/#tag/Time-Off/operation/getTimeOffRequest) |
| [Search Workspace Users](actions/search-workspace-users.md) | `POST workspaces/:workspaceId/users/info` | [docs](https://docs.developer.clockify.me/#tag/User/operation/filterUsersOfWorkspace) |
| [Stop User Running Timer](actions/stop-user-running-timer.md) | `PATCH workspaces/:workspaceId/user/:userId/time-entries` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/stopRunningTimeEntry) |
| [Submit Approval Request](actions/submit-approval-request.md) | `POST workspaces/:workspaceId/approval-requests` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/createApprrovalRequest) |
| [Submit User Approval Request](actions/submit-user-approval-request.md) | `POST workspaces/:workspaceId/approval-requests/users/:userId` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/createApprovalForOther) |
| [Update Approval Request](actions/update-approval-request.md) | `PATCH workspaces/:workspaceId/approval-requests/:approvalRequestId` | [docs](https://docs.developer.clockify.me/#tag/Approval/operation/updateApprovalStatus) |
| [Update Balance](actions/update-balance.md) | `PATCH workspaces/:workspaceId/time-off/balance/policy/:policyId` | [docs](https://docs.developer.clockify.me/#tag/Balance/operation/updateBalance) |
| [Update Expense](actions/update-expense.md) | `PUT workspaces/:workspaceId/expenses/:expenseId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/updateExpense) |
| [Update Expense Category](actions/update-expense-category.md) | `PUT workspaces/:workspaceId/expenses/categories/:categoryId` | [docs](https://docs.developer.clockify.me/#tag/Expense/operation/updateCategory) |
| [Update Group](actions/update-group.md) | `PUT workspaces/:workspaceId/user-groups/:id` | [docs](https://docs.developer.clockify.me/#tag/Group/operation/updateUserGroup) |
| [Update Holiday](actions/update-holiday.md) | `PUT workspaces/:workspaceId/holidays/:holidayId` | [docs](https://docs.developer.clockify.me/#tag/Holiday/operation/updateHoliday) |
| [Update Invoice](actions/update-invoice.md) | `PUT workspaces/:workspaceId/invoices/:invoiceId` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/updateInvoice) |
| [Update Invoice Settings](actions/update-invoice-settings.md) | `PUT workspaces/:workspaceId/invoices/settings` | [docs](https://docs.developer.clockify.me/#tag/Invoice/operation/updateInvoiceSettings) |
| [Update Member Profile](actions/update-member-profile.md) | `PATCH workspaces/:workspaceId/member-profile/:userId` | [docs](https://docs.developer.clockify.me/#tag/User/operation/updateMemberProfileWithAdditionalData) |
| [Update Policy](actions/update-policy.md) | `PUT workspaces/:workspaceId/time-off/policies/:id` | [docs](https://docs.developer.clockify.me/#tag/Policy/operation/updatePolicy) |
| [Update Project](actions/update-project.md) | `PUT workspaces/:workspaceId/projects/:projectId` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/updateProject) |
| [Update Project Custom Field](actions/update-project-custom-field.md) | `PATCH workspaces/:workspaceId/projects/:projectId/custom-fields/:customFieldId` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/editProjectCustomFieldDefaultValue) |
| [Update Project Estimate](actions/update-project-estimate.md) | `PATCH workspaces/:workspaceId/projects/:projectId/estimate` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/updateEstimate) |
| [Update Project Memberships](actions/update-project-memberships.md) | `PATCH workspaces/:workspaceId/projects/:projectId/memberships` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/updateMemberships) |
| [Update Project Task](actions/update-project-task.md) | `PUT workspaces/:workspaceId/projects/:projectId/tasks/:taskId` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/updateTask) |
| [Update Project Template](actions/update-project-template.md) | `PATCH workspaces/:workspaceId/projects/:projectId/template` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/updateIsProjectTemplate) |
| [Update Project User Cost Rate](actions/update-project-user-cost-rate.md) | `PUT workspaces/:workspaceId/projects/:projectId/users/:userId/cost-rate` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/addUsersCostRate) |
| [Update Project User Hourly Rate](actions/update-project-user-hourly-rate.md) | `PUT workspaces/:workspaceId/projects/:projectId/users/:userId/hourly-rate` | [docs](https://docs.developer.clockify.me/#tag/Project/operation/addUsersHourlyRate) |
| [Update Recurring Assignment](actions/update-recurring-assignment.md) | `PATCH workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId` | [docs](https://docs.developer.clockify.me/#tag/Scheduling/operation/editRecurring) |
| [Update Shared Report](actions/update-shared-report.md) | `PUT workspaces/:workspaceId/shared-reports/:id` | [docs](https://docs.developer.clockify.me/#tag/Shared-Report/operation/updateSharedReportV1) |
| [Update Tag](actions/update-tag.md) | `PUT workspaces/:workspaceId/tags/:id` | [docs](https://docs.developer.clockify.me/#tag/Tag/operation/updateTag) |
| [Update Task Cost Rate](actions/update-task-cost-rate.md) | `PUT workspaces/:workspaceId/projects/:projectId/tasks/:id/cost-rate` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/setTaskCostRate) |
| [Update Task Hourly Rate](actions/update-task-hourly-rate.md) | `PUT workspaces/:workspaceId/projects/:projectId/tasks/:id/hourly-rate` | [docs](https://docs.developer.clockify.me/#tag/Task/operation/setTaskHourlyRate) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT workspaces/:workspaceId/time-entries/:id` | [docs](https://docs.developer.clockify.me/#tag/Time-entry/operation/updateTimeEntry) |
| [Update User Cost Rate](actions/update-user-cost-rate.md) | `PUT workspaces/:workspaceId/users/:userId/cost-rate` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/setCostRateForUser) |
| [Update User Custom Field](actions/update-user-custom-field.md) | `PUT workspaces/:workspaceId/users/:userId/custom-field/:customFieldId/value` | [docs](https://docs.developer.clockify.me/#tag/User/operation/upsertUserCustomFieldValue) |
| [Update User Hourly Rate](actions/update-user-hourly-rate.md) | `PUT workspaces/:workspaceId/users/:userId/hourly-rate` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/setHourlyRateForUser) |
| [Update User Status](actions/update-user-status.md) | `PUT workspaces/:workspaceId/users/:userId` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/updateUserStatus) |
| [Update Webhook](actions/update-webhook.md) | `PUT workspaces/:workspaceId/webhooks/:webhookId` | [docs](https://docs.developer.clockify.me/#tag/Webhooks/operation/updateWebhook) |
| [Update Workspace Client](actions/update-workspace-client.md) | `PUT workspaces/:workspaceId/clients/:id` | [docs](https://docs.developer.clockify.me/#tag/Client/operation/updateClient) |
| [Update Workspace Cost Rate](actions/update-workspace-cost-rate.md) | `PUT workspaces/:workspaceId/cost-rate` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/setWorkspaceCostRate) |
| [Update Workspace Custom Field](actions/update-workspace-custom-field.md) | `PUT workspaces/:workspaceId/custom-fields/:customFieldId` | [docs](https://docs.developer.clockify.me/#tag/Custom-fields/operation/editCustomField) |
| [Update Workspace Hourly Rate](actions/update-workspace-hourly-rate.md) | `PUT workspaces/:workspaceId/hourly-rate` | [docs](https://docs.developer.clockify.me/#tag/Workspace/operation/setWorkspaceHourlyRate) |
| [Upload Image](actions/upload-image.md) | `POST file/image` | [docs](https://docs.developer.clockify.me/#tag/User/operation/uploadImage) |
