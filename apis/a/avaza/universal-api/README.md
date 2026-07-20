# <img src="https://images.mindcloud.co/apps/icons/avaza_1774030619648.png" alt="Avaza logo" width="28" height="28"> Avaza: Universal API

Manage projects, tasks, timesheets, expenses, invoices, and estimates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/avaza/latest
- **Category:** Productivity / Project Management
- **Actions:** 94
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.avaza.com
- **Vendor API docs:** https://api.avaza.com/swagger/ui/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (94)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Avaza. |

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | POST | Creates a new bill in Avaza. |
| [Get Bill](actions/get-bill.md) | GET | Retrieves bill from Avaza. |
| [List Bills](actions/list-bills.md) | GET | Retrieves bills from Avaza. |

### Bill Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill Payment](actions/create-bill-payment.md) | POST | Creates a new bill payment in Avaza. |
| [Get Bill Payment](actions/get-bill-payment.md) | GET | Retrieves bill payment from Avaza. |
| [List Bill Payments](actions/list-bill-payments.md) | GET | Retrieves bill payments from Avaza. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Avaza. |
| [Get Company](actions/get-company.md) | GET | Retrieves company from Avaza. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Avaza. |
| [List Companies Lookup](actions/list-companies-lookup.md) | GET | Retrieves companies lookup entries from Avaza. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Avaza. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Avaza. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact from Avaza. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Avaza. |

### Credit Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Note](actions/get-credit-note.md) | GET | Retrieves credit note from Avaza. |
| [List Credit Notes](actions/list-credit-notes.md) | GET | Retrieves credit notes from Avaza. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Avaza. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in Avaza. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves estimate from Avaza. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from Avaza. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Avaza. |
| [Create Expense Attachment](actions/create-expense-attachment.md) | POST | Uploads an expense attachment to Avaza. |
| [Delete Expense](actions/delete-expense.md) | DELETE | Deletes an existing expense from Avaza. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves expense from Avaza. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from Avaza. |
| [Submit Expenses for Approval](actions/submit-expenses-for-approval.md) | PUT | Submits expenses for approval in Avaza. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in Avaza. |

### Expense Category

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Categories](actions/list-expense-categories.md) | GET | Retrieves expense categories from Avaza. |

### Expense Group

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Groups Lookup](actions/list-expense-groups-lookup.md) | GET | Retrieves expense groups lookup entries from Avaza. |

### Expense Merchant

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Merchants Lookup](actions/list-expense-merchants-lookup.md) | GET | Retrieves expense merchants lookup entries from Avaza. |

### Expense Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Payment Methods Lookup](actions/list-expense-payment-methods-lookup.md) | GET | Retrieves expense payment methods lookup entries from Avaza. |

### Expense Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Expense Summary](actions/get-expense-summary.md) | GET | Retrieves aggregated expense data from Avaza. |

### Fixed Amount

| Action | Method | Description |
| --- | --- | --- |
| [List Fixed Amounts](actions/list-fixed-amounts.md) | GET | Retrieves fixed-amount entries from Avaza. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory](actions/get-inventory.md) | GET | Retrieves inventory from Avaza. |
| [List Inventories](actions/list-inventories.md) | GET | Retrieves inventory items from Avaza. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Avaza. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves invoice from Avaza. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Avaza. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Avaza. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in Avaza. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves payment from Avaza. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Avaza. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Avaza. |
| [Get Project](actions/get-project.md) | GET | Retrieves project from Avaza. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Avaza. |
| [List Projects Lookup](actions/list-projects-lookup.md) | GET | Retrieves projects lookup entries from Avaza. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Avaza. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Member](actions/create-project-member.md) | POST | Creates a new project member in Avaza. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Avaza. |
| [Update Project Member](actions/update-project-member.md) | PUT | Updates an existing project member in Avaza. |

### Project Timesheet Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Timesheet Category](actions/create-project-timesheet-category.md) | POST | Creates a new project timesheet category in Avaza. |
| [List Project Timesheet Categories](actions/list-project-timesheet-categories.md) | GET | Retrieves project timesheet categories from Avaza. |
| [Update Project Timesheet Category](actions/update-project-timesheet-category.md) | PUT | Updates an existing project timesheet category in Avaza. |

### Recurring Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Recurring Invoice](actions/get-recurring-invoice.md) | GET | Retrieves recurring invoice from Avaza. |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | GET | Retrieves recurring invoices from Avaza. |

### Schedule Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Schedule Assignments](actions/list-schedule-assignments.md) | GET | Retrieves schedule assignments from Avaza. |

### Schedule Series

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Booking](actions/create-leave-booking.md) | POST | Creates a leave booking in Avaza. |
| [Create Schedule Booking](actions/create-schedule-booking.md) | POST | Creates a project work booking in Avaza. |
| [Delete Schedule Series](actions/delete-schedule-series.md) | DELETE | Deletes an existing schedule series from Avaza. |
| [List Schedule Series](actions/list-schedule-series.md) | GET | Retrieves schedule series from Avaza. |
| [List Schedule Series By IDs](actions/list-schedule-series-by-ids.md) | GET | Retrieves schedule series by IDs from Avaza. |
| [Update Leave Booking](actions/update-leave-booking.md) | PUT | Updates an existing leave booking in Avaza. |
| [Update Schedule Booking](actions/update-schedule-booking.md) | PUT | Updates an existing schedule booking in Avaza. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Section](actions/create-section.md) | POST | Creates a new section in Avaza. |
| [Delete Section](actions/delete-section.md) | DELETE | Deletes an existing section from Avaza. |
| [List Sections](actions/list-sections.md) | GET | Retrieves sections from Avaza. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Avaza. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Avaza. |
| [Get Task](actions/get-task.md) | GET | Retrieves task from Avaza. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Avaza. |
| [List Tasks Lookup](actions/list-tasks-lookup.md) | GET | Retrieves tasks lookup entries from Avaza. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Avaza. |

### Task Discussion

| Action | Method | Description |
| --- | --- | --- |
| [List Task Discussions](actions/list-task-discussions.md) | GET | Retrieves task discussion messages from Avaza. |

### Task Status

| Action | Method | Description |
| --- | --- | --- |
| [List Task Statuses](actions/list-task-statuses.md) | GET | Retrieves task statuses from Avaza. |

### Task Type

| Action | Method | Description |
| --- | --- | --- |
| [List Task Types](actions/list-task-types.md) | GET | Retrieves task types from Avaza. |

### Tax

| Action | Method | Description |
| --- | --- | --- |
| [List Taxes](actions/list-taxes.md) | GET | Retrieves taxes from Avaza. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST | Creates a new timesheet in Avaza. |
| [Delete Timesheet](actions/delete-timesheet.md) | DELETE | Deletes an existing timesheet from Avaza. |
| [Get Timesheet](actions/get-timesheet.md) | GET | Retrieves timesheet from Avaza. |
| [List Deleted Timesheets](actions/list-deleted-timesheets.md) | GET | Retrieves deleted timesheet entries from Avaza. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from Avaza. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates an existing timesheet in Avaza. |

### Timesheet Submission

| Action | Method | Description |
| --- | --- | --- |
| [Submit Timesheets for Approval](actions/submit-timesheets-for-approval.md) | PUT | Submits timesheets for approval in Avaza. |

### Timesheet Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Timesheet Summary](actions/get-timesheet-summary.md) | GET | Retrieves aggregated timesheet data from Avaza. |

### Timesheet Timer

| Action | Method | Description |
| --- | --- | --- |
| [Get Running Timesheet Timer](actions/get-running-timesheet-timer.md) | GET | Retrieves the running timesheet timer from Avaza. |
| [Start Timesheet Timer](actions/start-timesheet-timer.md) | PUT | Starts a timesheet timer in Avaza. |
| [Stop Timesheet Timer](actions/stop-timesheet-timer.md) | PUT | Stops a running timesheet timer in Avaza. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [List User Profiles](actions/list-user-profiles.md) | GET | Retrieves user profiles from Avaza. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Avaza. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Avaza. |
| [Delete Webhook By URL](actions/delete-webhook-by-url.md) | DELETE | Deletes a webhook from Avaza by callback URL. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook from Avaza. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Avaza. |

