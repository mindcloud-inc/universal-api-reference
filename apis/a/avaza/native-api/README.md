# Avaza: Native API Reference

A consolidated summary of Avaza's API configuration and 94 documented operations, with links to official documentation.

- **Official docs:** https://api.avaza.com/swagger/ui/index
- **OpenAPI specification:** https://api.avaza.com/swagger/docs/v1
- **API base URL:** `https://api.avaza.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://any.avaza.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://any.avaza.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read_account read_contacts write_contacts read_projects write_projects read_financials write_financials read_expenses write_expenses read_timesheets write_timesheets read_schedule write_schedule webhook_notifications`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://any.avaza.com/oauth2/token.

[Official authentication documentation](https://www.avaza.com/avaza-api-oauth2-authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `Sort` in the query string. Use `ascending` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (94 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | `POST /api/Bill` | [docs](https://api.avaza.com/#!/Bill/Bill_Post) |
| [Create Bill Payment](actions/create-bill-payment.md) | `POST /api/BillPayment` | [docs](https://api.avaza.com/#!/BillPayment/BillPayment_Post) |
| [Create Company](actions/create-company.md) | `POST /api/Company` | [docs](https://api.avaza.com/#!/Company/Company_Post) |
| [Create Contact](actions/create-contact.md) | `POST /api/Contact` | [docs](https://api.avaza.com/#!/Contact/Contact_Post) |
| [Create Estimate](actions/create-estimate.md) | `POST /api/Estimate` | [docs](https://api.avaza.com/#!/Estimate/Estimate_Post) |
| [Create Expense](actions/create-expense.md) | `POST /api/Expense` | [docs](https://api.avaza.com/#!/Expense/Expense_Post) |
| [Create Expense Attachment](actions/create-expense-attachment.md) | `POST /api/Expense/Attachment` | [docs](https://api.avaza.com/#!/Expense/ExpenseAttachment) |
| [Create Invoice](actions/create-invoice.md) | `POST /api/Invoice` | [docs](https://api.avaza.com/#!/Invoice/Invoice_Post) |
| [Create Leave Booking](actions/create-leave-booking.md) | `POST /ScheduleSeries/AddLeave` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_AddLeave) |
| [Create Payment](actions/create-payment.md) | `POST /api/Payment` | [docs](https://api.avaza.com/#!/Payment/Payment_Post) |
| [Create Project](actions/create-project.md) | `POST /api/Project` | [docs](https://api.avaza.com/#!/Project/Project_Post) |
| [Create Project Member](actions/create-project-member.md) | `POST /api/ProjectMember` | [docs](https://api.avaza.com/#!/ProjectMember/ProjectMember_Post) |
| [Create Project Timesheet Category](actions/create-project-timesheet-category.md) | `POST /api/ProjectTimesheetCategory` | [docs](https://api.avaza.com/#!/ProjectTimesheetCategory/ProjectTimesheetCategory_Post) |
| [Create Schedule Booking](actions/create-schedule-booking.md) | `POST /ScheduleSeries/AddBooking` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_AddBooking) |
| [Create Section](actions/create-section.md) | `POST /api/Section` | [docs](https://api.avaza.com/#!/Section/Section_Post) |
| [Create Task](actions/create-task.md) | `POST /api/Task` | [docs](https://api.avaza.com/#!/Task/Task_Post) |
| [Create Timesheet](actions/create-timesheet.md) | `POST /api/Timesheet` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_Post) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/Webhook` | [docs](https://api.avaza.com/#!/Webhook/Webhook_Post) |
| [Delete Expense](actions/delete-expense.md) | `DELETE /api/Expense` | [docs](https://api.avaza.com/#!/Expense/Expense_Delete) |
| [Delete Schedule Series](actions/delete-schedule-series.md) | `DELETE /api/ScheduleSeries/:id` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_Delete) |
| [Delete Section](actions/delete-section.md) | `DELETE /api/Section` | [docs](https://api.avaza.com/#!/Section/Section_Delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/Task` | [docs](https://api.avaza.com/#!/Task/Task_Delete) |
| [Delete Timesheet](actions/delete-timesheet.md) | `DELETE /api/Timesheet/:id` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_Delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/Webhook/:id` | [docs](https://api.avaza.com/#!/Webhook/Webhook_Delete) |
| [Delete Webhook By URL](actions/delete-webhook-by-url.md) | `DELETE /api/Webhook` | [docs](https://api.avaza.com/#!/Webhook/Webhook_DeleteByUrl) |
| [Get Account Details](actions/get-account-details.md) | `GET /api/Account` | [docs](https://api.avaza.com/#!/Account/Account_Get) |
| [Get Bill](actions/get-bill.md) | `GET /api/Bill/:id` | [docs](https://api.avaza.com/#!/Bill/Bill_GetByID) |
| [Get Bill Payment](actions/get-bill-payment.md) | `GET /api/BillPayment/:id` | [docs](https://api.avaza.com/#!/BillPayment/BillPayment_GetByID) |
| [Get Company](actions/get-company.md) | `GET /api/Company/:id` | [docs](https://api.avaza.com/#!/Company/Company_GetByID) |
| [Get Contact](actions/get-contact.md) | `GET /api/Contact/:id` | [docs](https://api.avaza.com/#!/Contact/Contact_GetByID) |
| [Get Credit Note](actions/get-credit-note.md) | `GET /api/CreditNote/:id` | [docs](https://api.avaza.com/#!/CreditNote/CreditNote_GetByID) |
| [Get Estimate](actions/get-estimate.md) | `GET /api/Estimate/:id` | [docs](https://api.avaza.com/#!/Estimate/Estimate_GetByID) |
| [Get Expense](actions/get-expense.md) | `GET /api/Expense/:id` | [docs](https://api.avaza.com/#!/Expense/Expense_GetByID) |
| [Get Expense Summary](actions/get-expense-summary.md) | `GET /api/ExpenseSummary` | [docs](https://api.avaza.com/#!/ExpenseSummary/ExpenseSummary_Get) |
| [Get Inventory](actions/get-inventory.md) | `GET /api/Inventory/:id` | [docs](https://api.avaza.com/#!/Inventory/Inventory_GetByID) |
| [Get Invoice](actions/get-invoice.md) | `GET /api/Invoice/:id` | [docs](https://api.avaza.com/#!/Invoice/Invoice_GetByID) |
| [Get Payment](actions/get-payment.md) | `GET /api/Payment/:id` | [docs](https://api.avaza.com/#!/Payment/Payment_GetByID) |
| [Get Project](actions/get-project.md) | `GET /api/Project/:id` | [docs](https://api.avaza.com/#!/Project/Project_GetByID) |
| [Get Recurring Invoice](actions/get-recurring-invoice.md) | `GET /api/RecurringInvoice/:id` | [docs](https://api.avaza.com/#!/RecurringInvoice/RecurringInvoice_GetByID) |
| [Get Running Timesheet Timer](actions/get-running-timesheet-timer.md) | `GET /api/TimesheetTimer` | [docs](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_GetRunningTimer) |
| [Get Task](actions/get-task.md) | `GET /api/Task/:id` | [docs](https://api.avaza.com/#!/Task/Task_GetByID) |
| [Get Timesheet](actions/get-timesheet.md) | `GET /api/Timesheet/:id` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_GetByID) |
| [Get Timesheet Summary](actions/get-timesheet-summary.md) | `GET /api/TimesheetSummary` | [docs](https://api.avaza.com/#!/TimesheetSummary/TimesheetSummary_Get) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/Webhook/:id` | [docs](https://api.avaza.com/#!/Webhook/Webhook_GetByID) |
| [List Bill Payments](actions/list-bill-payments.md) | `GET /api/BillPayment` | [docs](https://api.avaza.com/#!/BillPayment/BillPayment_Get) |
| [List Bills](actions/list-bills.md) | `GET /api/Bill` | [docs](https://api.avaza.com/#!/Bill/Bill_Get) |
| [List Companies](actions/list-companies.md) | `GET /api/Company` | [docs](https://api.avaza.com/#!/Company/Company_Get) |
| [List Companies Lookup](actions/list-companies-lookup.md) | `GET /api/Company/Lookup` | [docs](https://api.avaza.com/#!/Company/CompanyLookup) |
| [List Contacts](actions/list-contacts.md) | `GET /api/Contact` | [docs](https://api.avaza.com/#!/Contact/Contact_Get) |
| [List Credit Notes](actions/list-credit-notes.md) | `GET /api/CreditNote` | [docs](https://api.avaza.com/#!/CreditNote/CreditNote_Get) |
| [List Currencies](actions/list-currencies.md) | `GET /api/Currency` | [docs](https://api.avaza.com/#!/Currency/Currency_Get) |
| [List Deleted Timesheets](actions/list-deleted-timesheets.md) | `GET /api/Timesheet/deleted` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_GetDeletedTimesheets) |
| [List Estimates](actions/list-estimates.md) | `GET /api/Estimate` | [docs](https://api.avaza.com/#!/Estimate/Estimate_Get) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET /api/ExpenseCategory` | [docs](https://api.avaza.com/#!/ExpenseCategory/ExpenseCategory_Get) |
| [List Expense Groups Lookup](actions/list-expense-groups-lookup.md) | `GET /api/ExpenseGroup/Lookup` | [docs](https://api.avaza.com/#!/ExpenseGroup/ExpenseGroupLookup) |
| [List Expense Merchants Lookup](actions/list-expense-merchants-lookup.md) | `GET /api/ExpenseMerchant/Lookup` | [docs](https://api.avaza.com/#!/ExpenseMerchant/ExpenseMerchangeLookup) |
| [List Expense Payment Methods Lookup](actions/list-expense-payment-methods-lookup.md) | `GET /api/ExpensePaymentMethod/Lookup` | [docs](https://api.avaza.com/#!/ExpensePaymentMethod/ExpensePaymentMethodLookup) |
| [List Expenses](actions/list-expenses.md) | `GET /api/Expense` | [docs](https://api.avaza.com/#!/Expense/Expense_Get) |
| [List Fixed Amounts](actions/list-fixed-amounts.md) | `GET /api/FixedAmount` | [docs](https://api.avaza.com/#!/FixedAmount/FixedAmount_Get) |
| [List Inventories](actions/list-inventories.md) | `GET /api/Inventory` | [docs](https://api.avaza.com/#!/Inventory/Inventory_Get) |
| [List Invoices](actions/list-invoices.md) | `GET /api/Invoice` | [docs](https://api.avaza.com/#!/Invoice/Invoice_Get) |
| [List Payments](actions/list-payments.md) | `GET /api/Payment` | [docs](https://api.avaza.com/#!/Payment/Payment_Get) |
| [List Project Members](actions/list-project-members.md) | `GET /api/ProjectMember` | [docs](https://api.avaza.com/#!/ProjectMember/ProjectMember_Get) |
| [List Project Timesheet Categories](actions/list-project-timesheet-categories.md) | `GET /api/ProjectTimesheetCategory` | [docs](https://api.avaza.com/#!/ProjectTimesheetCategory/ProjectTimesheetCategory_Get) |
| [List Projects](actions/list-projects.md) | `GET /api/Project` | [docs](https://api.avaza.com/#!/Project/Project_Get) |
| [List Projects Lookup](actions/list-projects-lookup.md) | `GET /api/Project/Lookup` | [docs](https://api.avaza.com/#!/Project/ProjectLookup) |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | `GET /api/RecurringInvoice` | [docs](https://api.avaza.com/#!/RecurringInvoice/RecurringInvoice_Get) |
| [List Schedule Assignments](actions/list-schedule-assignments.md) | `GET /api/ScheduleAssignment` | [docs](https://api.avaza.com/#!/ScheduleAssignment/ScheduleAssignment_Get) |
| [List Schedule Series](actions/list-schedule-series.md) | `GET /api/ScheduleSeries` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_Get) |
| [List Schedule Series By IDs](actions/list-schedule-series-by-ids.md) | `POST /api/ScheduleSeries` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_GetByFilter) |
| [List Sections](actions/list-sections.md) | `GET /api/Section` | [docs](https://api.avaza.com/#!/Section/Section_Get) |
| [List Task Discussions](actions/list-task-discussions.md) | `GET /api/TaskDiscussion` | [docs](https://api.avaza.com/#!/TaskDiscussion/TaskDiscussion_Get) |
| [List Task Statuses](actions/list-task-statuses.md) | `GET /api/TaskStatus` | [docs](https://api.avaza.com/#!/TaskStatus/TaskStatus_Get) |
| [List Task Types](actions/list-task-types.md) | `GET /api/TaskType` | [docs](https://api.avaza.com/#!/TaskType/TaskType_Get) |
| [List Tasks](actions/list-tasks.md) | `GET /api/Task` | [docs](https://api.avaza.com/#!/Task/Task_Get) |
| [List Tasks Lookup](actions/list-tasks-lookup.md) | `GET /api/Task/Lookup` | [docs](https://api.avaza.com/#!/Task/TaskLookup) |
| [List Taxes](actions/list-taxes.md) | `GET /api/Tax` | [docs](https://api.avaza.com/#!/Tax/Tax_Get) |
| [List Timesheets](actions/list-timesheets.md) | `GET /api/Timesheet` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_Get) |
| [List User Profiles](actions/list-user-profiles.md) | `GET /api/UserProfile` | [docs](https://api.avaza.com/#!/UserProfile/UserProfile_Get) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/Webhook` | [docs](https://api.avaza.com/#!/Webhook/Webhook_Get) |
| [Start Timesheet Timer](actions/start-timesheet-timer.md) | `POST /api/TimesheetTimer/:id` | [docs](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_StartTimer) |
| [Stop Timesheet Timer](actions/stop-timesheet-timer.md) | `DELETE /api/TimesheetTimer/:id` | [docs](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_StopTimer) |
| [Submit Expenses for Approval](actions/submit-expenses-for-approval.md) | `POST /api/ExpenseApproval/Submit` | [docs](https://api.avaza.com/#!/Expense/ExpenseApproval) |
| [Submit Timesheets for Approval](actions/submit-timesheets-for-approval.md) | `POST /api/TimesheetSubmission` | [docs](https://api.avaza.com/#!/TimesheetSubmission/TimesheetSubmission_Post) |
| [Update Company](actions/update-company.md) | `PUT /api/Company` | [docs](https://api.avaza.com/#!/Company/Company_Put) |
| [Update Expense](actions/update-expense.md) | `PUT /api/Expense` | [docs](https://api.avaza.com/#!/Expense/Expense_Put) |
| [Update Invoice](actions/update-invoice.md) | `PUT /api/Invoice` | [docs](https://api.avaza.com/#!/Invoice/Invoice_Put) |
| [Update Leave Booking](actions/update-leave-booking.md) | `PUT /ScheduleSeries/EditLeave` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_EditLeave) |
| [Update Project](actions/update-project.md) | `PUT /api/Project` | [docs](https://api.avaza.com/#!/Project/Project_Put) |
| [Update Project Member](actions/update-project-member.md) | `PUT /api/ProjectMember` | [docs](https://api.avaza.com/#!/ProjectMember/ProjectMember_Put) |
| [Update Project Timesheet Category](actions/update-project-timesheet-category.md) | `PUT /api/ProjectTimesheetCategory` | [docs](https://api.avaza.com/#!/ProjectTimesheetCategory/ProjectTimesheetCategory_Put) |
| [Update Schedule Booking](actions/update-schedule-booking.md) | `PUT /ScheduleSeries/EditBooking` | [docs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_EditBooking) |
| [Update Task](actions/update-task.md) | `PUT /api/Task` | [docs](https://api.avaza.com/#!/Task/Task_Put) |
| [Update Timesheet](actions/update-timesheet.md) | `PUT /api/Timesheet` | [docs](https://api.avaza.com/#!/Timesheet/Timesheet_Put) |
