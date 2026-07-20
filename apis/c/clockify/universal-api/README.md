# <img src="https://images.mindcloud.co/apps/icons/clockify_1771877968585.png" alt="Clockify logo" width="28" height="28"> Clockify: Universal API

Track time, manage projects, approve timesheets, and analyze team costs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clockify/latest
- **Category:** Human Resources / HRIS
- **Actions:** 154
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clockify.me/
- **Vendor API docs:** https://docs.developer.clockify.me/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (154)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Client](actions/create-workspace-client.md) | POST | Creates a new workspace client in Clockify. |
| [List Workspace Clients](actions/list-workspace-clients.md) | GET | Lists all workspace clients in Clockify. |
| [Update Workspace Client](actions/update-workspace-client.md) | PUT | Updates an existing workspace client in Clockify. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Users to Group](actions/add-users-to-group.md) | PUT | Adds users to a group in Clockify. |
| [Create Group](actions/create-group.md) | POST | Creates a new user group in Clockify. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing user group from Clockify. |
| [Remove User from Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a group in Clockify. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing user group in Clockify. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Manager Role to User](actions/add-manager-role-to-user.md) | POST | Adds the manager role to a user in Clockify. |
| [Add User to Workspace](actions/add-user-to-workspace.md) | POST | Adds a user to a workspace in Clockify. |
| [Archive Expense Category](actions/archive-expense-category.md) | PUT | Archives an expense category in Clockify. |
| [Change Invoice Status](actions/change-invoice-status.md) | PUT | Updates an invoice status in Clockify. |
| [Change Policy Status](actions/change-policy-status.md) | PUT | Updates a policy status in Clockify. |
| [Change Time Off Request Status](actions/change-time-off-request-status.md) | PUT | Updates a time off request status in Clockify. |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Clockify. |
| [Create Expense Category](actions/create-expense-category.md) | POST | Creates a new expense category in Clockify. |
| [Create Holiday](actions/create-holiday.md) | POST | Creates a new holiday in Clockify. |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Clockify. |
| [Create Invoice Payment](actions/create-invoice-payment.md) | POST | Creates a new invoice payment in Clockify. |
| [Create Time Off Policy](actions/create-time-off-policy.md) | POST | Creates a time off policy in Clockify. |
| [Create Time Off Request](actions/create-time-off-request.md) | POST | Creates a time off request in Clockify. |
| [Create User Time Entry](actions/create-user-time-entry.md) | POST | Creates a time entry for a user in Clockify. |
| [Create User Time Off Request](actions/create-user-time-off-request.md) | POST | Creates a time off request for a user in Clockify. |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Clockify. |
| [Create Workspace Custom Field](actions/create-workspace-custom-field.md) | POST | Creates a workspace custom field in Clockify. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Clockify. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from Clockify. |
| [Delete Expense](actions/delete-expense.md) | DELETE | Deletes an existing expense from Clockify. |
| [Delete Expense Category](actions/delete-expense-category.md) | DELETE | Deletes an existing expense category from Clockify. |
| [Delete Holiday](actions/delete-holiday.md) | DELETE | Deletes an existing holiday from Clockify. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Clockify. |
| [Delete Invoice Payment](actions/delete-invoice-payment.md) | DELETE | Deletes an existing invoice payment from Clockify. |
| [Delete Policy](actions/delete-policy.md) | DELETE | Deletes an existing policy from Clockify. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Clockify. |
| [Delete Project Task](actions/delete-project-task.md) | DELETE | Deletes an existing project task from Clockify. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Clockify. |
| [Delete Time Off Request](actions/delete-time-off-request.md) | DELETE | Deletes a time off request from Clockify. |
| [Delete User Time Entries](actions/delete-user-time-entries.md) | DELETE | Deletes a user's time entries from Clockify. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Clockify. |
| [Delete Workspace Time Entry](actions/delete-workspace-time-entry.md) | DELETE | Deletes a workspace time entry from Clockify. |
| [Download Receipt](actions/download-receipt.md) | GET | Downloads an expense receipt from Clockify. |
| [Duplicate Invoice](actions/duplicate-invoice.md) | POST | Duplicates an existing invoice in Clockify. |
| [Duplicate Time Entry](actions/duplicate-time-entry.md) | POST | Duplicates an existing time entry in Clockify. |
| [Export Invoice](actions/export-invoice.md) | GET | Exports a workspace invoice from Clockify. |
| [Generate Webhook Token](actions/generate-webhook-token.md) | PUT | Generates a new webhook token in Clockify. |
| [Get Client](actions/get-client.md) | GET | Retrieves a specific client from Clockify. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves a specific expense from Clockify. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves a specific invoice from Clockify. |
| [Get Invoice Settings](actions/get-invoice-settings.md) | GET | Retrieves workspace invoice settings from Clockify. |
| [Get Member Profile](actions/get-member-profile.md) | GET | Retrieves a member profile from Clockify. |
| [Get Policy Balances](actions/get-policy-balances.md) | GET | Retrieves time off policy balances from Clockify. |
| [Get Project Task](actions/get-project-task.md) | GET | Retrieves a specific project task from Clockify. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from Clockify. |
| [Get Time Off Policy](actions/get-time-off-policy.md) | GET | Retrieves a time off policy from Clockify. |
| [Get User Balance](actions/get-user-balance.md) | GET | Retrieves a user's time off balance from Clockify. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a specific webhook from Clockify. |
| [Get Webhook Logs](actions/get-webhook-logs.md) | GET | Retrieves logs for a webhook from Clockify. |
| [Get Workspace Time Entry](actions/get-workspace-time-entry.md) | GET | Retrieves a workspace time entry from Clockify. |
| [List Addon Webhooks](actions/list-addon-webhooks.md) | GET | Lists all addon webhooks in Clockify. |
| [List Approval Requests](actions/list-approval-requests.md) | GET | Lists all approval requests in Clockify. |
| [List Assignments](actions/list-assignments.md) | GET | Lists all scheduling assignments in Clockify. |
| [List Created Entities (Experimental)](actions/list-created-entities-experimental.md) | GET | Lists experimentally tracked created entities in Clockify. |
| [List Deleted Entities (Experimental)](actions/list-deleted-entities-experimental.md) | GET | Lists experimentally tracked deleted entities in Clockify. |
| [List Expense Categories](actions/list-expense-categories.md) | GET | Lists all expense categories in Clockify. |
| [List Holidays in Period](actions/list-holidays-in-period.md) | GET | Lists holidays in a period in Clockify. |
| [List Invoice Payments](actions/list-invoice-payments.md) | GET | Lists all invoice payments in Clockify. |
| [List Project Custom Fields](actions/list-project-custom-fields.md) | GET | Lists all project custom fields in Clockify. |
| [List Updated Entities (Experimental)](actions/list-updated-entities-experimental.md) | GET | Lists experimentally tracked updated entities in Clockify. |
| [List User Groups](actions/list-user-groups.md) | GET | Lists all user groups in Clockify. |
| [List User Managers](actions/list-user-managers.md) | GET | Lists all user managers in Clockify. |
| [List Workspace Custom Fields](actions/list-workspace-custom-fields.md) | GET | Lists all workspace custom fields in Clockify. |
| [List Workspace Expenses](actions/list-workspace-expenses.md) | GET | Lists all workspace expenses in Clockify. |
| [List Workspace Holidays](actions/list-workspace-holidays.md) | GET | Lists all workspace holidays in Clockify. |
| [List Workspace Invoices](actions/list-workspace-invoices.md) | GET | Lists all workspace invoices in Clockify. |
| [List Workspace Policies](actions/list-workspace-policies.md) | GET | Lists all workspace policies in Clockify. |
| [List Workspace Webhooks](actions/list-workspace-webhooks.md) | GET | Lists all workspace webhooks in Clockify. |
| [Mark Time Entries as Invoiced](actions/mark-time-entries-as-invoiced.md) | PUT | Marks time entries as invoiced in Clockify. |
| [Remove Manager Role from User](actions/remove-manager-role-from-user.md) | DELETE | Removes the manager role from a user in Clockify. |
| [Remove Project Custom Field](actions/remove-project-custom-field.md) | DELETE | Removes a project custom field in Clockify. |
| [Replace Time Entries](actions/replace-time-entries.md) | PUT | Replaces a user's time entries in Clockify. |
| [Resubmit Entries and Expenses for Approval](actions/resubmit-entries-and-expenses-for-approval.md) | POST | Resubmits entries and expenses for approval in Clockify. |
| [Resubmit User Entries and Expenses for Approval](actions/resubmit-user-entries-and-expenses-for-approval.md) | POST | Resubmits a user's entries and expenses for approval in Clockify. |
| [Search Invoices](actions/search-invoices.md) | GET | Finds invoices in Clockify by filters. |
| [Search Workspace Time Off Requests](actions/search-workspace-time-off-requests.md) | GET | Finds workspace time off requests in Clockify by filters. |
| [Stop User Running Timer](actions/stop-user-running-timer.md) | PUT | Stops a user's running timer in Clockify. |
| [Submit Approval Request](actions/submit-approval-request.md) | POST | Submits an approval request in Clockify. |
| [Submit User Approval Request](actions/submit-user-approval-request.md) | POST | Submits an approval request for a user in Clockify. |
| [Update Approval Request](actions/update-approval-request.md) | PUT | Updates an approval request in Clockify. |
| [Update Balance](actions/update-balance.md) | PUT | Updates a time off balance in Clockify. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in Clockify. |
| [Update Expense Category](actions/update-expense-category.md) | PUT | Updates an existing expense category in Clockify. |
| [Update Holiday](actions/update-holiday.md) | PUT | Updates an existing holiday in Clockify. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Clockify. |
| [Update Invoice Settings](actions/update-invoice-settings.md) | PUT | Updates workspace invoice settings in Clockify. |
| [Update Member Profile](actions/update-member-profile.md) | PUT | Updates a member profile in Clockify. |
| [Update Policy](actions/update-policy.md) | PUT | Updates an existing policy in Clockify. |
| [Update Project Custom Field](actions/update-project-custom-field.md) | PUT | Updates a project custom field in Clockify. |
| [Update Project Estimate](actions/update-project-estimate.md) | PUT | Updates a project estimate in Clockify. |
| [Update Project Memberships](actions/update-project-memberships.md) | PUT | Updates workspace project memberships in Clockify. |
| [Update Project Template](actions/update-project-template.md) | PUT | Updates a project template in Clockify. |
| [Update Project User Cost Rate](actions/update-project-user-cost-rate.md) | PUT | Updates a project user cost rate in Clockify. |
| [Update Project User Hourly Rate](actions/update-project-user-hourly-rate.md) | PUT | Updates a project user hourly rate in Clockify. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Clockify. |
| [Update Task Cost Rate](actions/update-task-cost-rate.md) | PUT | Updates a task cost rate in Clockify. |
| [Update Task Hourly Rate](actions/update-task-hourly-rate.md) | PUT | Updates a task hourly rate in Clockify. |
| [Update User Cost Rate](actions/update-user-cost-rate.md) | PUT | Updates a user cost rate in Clockify. |
| [Update User Custom Field](actions/update-user-custom-field.md) | PUT | Updates a user custom field value in Clockify. |
| [Update User Hourly Rate](actions/update-user-hourly-rate.md) | PUT | Updates a user hourly rate in Clockify. |
| [Update User Status](actions/update-user-status.md) | PUT | Updates a user status in Clockify. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Clockify. |
| [Update Workspace Cost Rate](actions/update-workspace-cost-rate.md) | PUT | Updates a workspace cost rate in Clockify. |
| [Update Workspace Custom Field](actions/update-workspace-custom-field.md) | PUT | Updates a workspace custom field in Clockify. |
| [Update Workspace Hourly Rate](actions/update-workspace-hourly-rate.md) | PUT | Updates a workspace hourly rate in Clockify. |
| [Upload Image](actions/upload-image.md) | POST | Uploads a user image to Clockify. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Add Users to Project](actions/add-users-to-project.md) | PUT | Adds users to a project in Clockify. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Clockify. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a specific workspace from Clockify. |
| [Get Workspace Project](actions/get-workspace-project.md) | GET | Retrieves a specific workspace project from Clockify. |
| [List Workspace Projects](actions/list-workspace-projects.md) | GET | Lists all workspace projects in Clockify. |
| [List Workspaces](actions/list-workspaces.md) | GET | Lists all available workspaces in Clockify. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Clockify. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Shared Report](actions/create-shared-report.md) | POST | Creates a new shared report in Clockify. |
| [Delete Shared Report](actions/delete-shared-report.md) | DELETE | Deletes an existing shared report from Clockify. |
| [Generate Attendance Report](actions/generate-attendance-report.md) | GET | Generates an attendance report in Clockify. |
| [Generate Detailed Report](actions/generate-detailed-report.md) | GET | Generates a detailed report in Clockify. |
| [Generate Expense Report](actions/generate-expense-report.md) | GET | Generates an expense report in Clockify. |
| [Generate Shared Report](actions/generate-shared-report.md) | GET | Generates a shared report in Clockify. |
| [Generate Summary Report](actions/generate-summary-report.md) | GET | Generates a summary report in Clockify. |
| [Generate Weekly Report](actions/generate-weekly-report.md) | GET | Generates a weekly report in Clockify. |
| [List My Shared Reports](actions/list-my-shared-reports.md) | GET | Lists your shared reports in Clockify. |
| [Update Shared Report](actions/update-shared-report.md) | PUT | Updates an existing shared report in Clockify. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Tag](actions/create-workspace-tag.md) | POST | Creates a new workspace tag in Clockify. |
| [List Workspace Tags](actions/list-workspace-tags.md) | GET | Lists all workspace tags in Clockify. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task](actions/create-project-task.md) | POST | Creates a new project task in Clockify. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Lists all project tasks in Clockify. |
| [Update Project Task](actions/update-project-task.md) | PUT | Updates an existing project task in Clockify. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Clockify. |
| [List In-Progress Time Entries](actions/list-in-progress-time-entries.md) | GET | Lists in-progress time entries in Clockify. |
| [List User Time Entries](actions/list-user-time-entries.md) | GET | Lists a user's time entries in Clockify. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Clockify. |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Change Recurring Period](actions/change-recurring-period.md) | PUT | Updates a recurring assignment period in Clockify. |
| [Copy Scheduled Assignment](actions/copy-scheduled-assignment.md) | POST | Copies a scheduled assignment in Clockify. |
| [Create Recurring Assignment](actions/create-recurring-assignment.md) | POST | Creates a recurring assignment in Clockify. |
| [Delete Recurring Assignment](actions/delete-recurring-assignment.md) | DELETE | Deletes a recurring assignment from Clockify. |
| [Get Filtered Project Totals](actions/get-filtered-project-totals.md) | GET | Retrieves filtered project totals from Clockify. |
| [Get Project Totals](actions/get-project-totals.md) | GET | Retrieves project totals for one project from Clockify. |
| [Get Workspace User Capacity Total](actions/get-workspace-user-capacity-total.md) | GET | Retrieves a workspace user capacity total from Clockify. |
| [Get Workspace User Capacity Totals](actions/get-workspace-user-capacity-totals.md) | GET | Retrieves workspace user capacity totals from Clockify. |
| [Publish Assignments](actions/publish-assignments.md) | PUT | Publishes workspace scheduling assignments in Clockify. |
| [Update Recurring Assignment](actions/update-recurring-assignment.md) | PUT | Updates a recurring assignment in Clockify. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Clockify. |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Lists all workspace users in Clockify. |
| [Search Workspace Users](actions/search-workspace-users.md) | GET | Finds workspace users in Clockify by filters. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Clockify. |

