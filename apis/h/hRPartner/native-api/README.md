# HR Partner: Native API Reference

A consolidated summary of HR Partner's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.hrpartner.io
- **API base URL:** `https://api.hrpartner.io`

## Authentication

### API Key

Use your HR Partner API key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developer.hrpartner.io/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add or Update Applicant](actions/add-or-update-applicant.md) | `POST /applicant` | [docs](https://developer.hrpartner.io/#add-or-update-an-applicant) |
| [Add or Update Application](actions/add-or-update-application.md) | `POST /application` | [docs](https://developer.hrpartner.io/#add-or-update-an-application) |
| [Add or Update Employee](actions/add-or-update-employee.md) | `POST /employee` | [docs](https://developer.hrpartner.io/#update-add-an-employee) |
| [Add Timeclock Entry](actions/add-timeclock-entry.md) | `POST /timeclock` | [docs](https://developer.hrpartner.io/#add-a-timesheet-timeclock-entry) |
| [Get Applicant](actions/get-applicant.md) | `GET /applicant/:applicantID` | [docs](https://developer.hrpartner.io/#get-a-specific-applicant) |
| [Get Application](actions/get-application.md) | `GET /application/:applicationID` | [docs](https://developer.hrpartner.io/#get-a-specific-application) |
| [Get Application Stage Tracking](actions/get-application-stage-tracking.md) | `GET /stage/track` | [docs](https://developer.hrpartner.io/#get-application-stage-tracking) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://developer.hrpartner.io/#company) |
| [Get Employee](actions/get-employee.md) | `GET /employee/:employeeCode` | [docs](https://developer.hrpartner.io/#get-a-specific-employee) |
| [Get Job Listing](actions/get-job-listing.md) | `GET /job/:jobID` | [docs](https://developer.hrpartner.io/#get-a-specific-job-listing) |
| [Get Leave Request](actions/get-leave-request.md) | `GET /leave_request/:leaverequestID` | [docs](https://developer.hrpartner.io/#get-a-specific-leave-request) |
| [Get Reminder](actions/get-reminder.md) | `GET /reminder/:reminderID` | [docs](https://developer.hrpartner.io/#get-a-specific-reminder) |
| [Get Timesheet](actions/get-timesheet.md) | `GET /singletimesheet` | [docs](https://developer.hrpartner.io/#get-a-single-timesheet) |
| [List Absences](actions/list-absences.md) | `GET /absences` | [docs](https://developer.hrpartner.io/#absences) |
| [List Applicants](actions/list-applicants.md) | `GET /applicants` | [docs](https://developer.hrpartner.io/#get-all-applicants) |
| [List Applications](actions/list-applications.md) | `GET /applications/:jobID` | [docs](https://developer.hrpartner.io/#get-all-applications) |
| [List Assets](actions/list-assets.md) | `GET /assets` | [docs](https://developer.hrpartner.io/#assets) |
| [List Benefits](actions/list-benefits.md) | `GET /benefits` | [docs](https://developer.hrpartner.io/#benefits) |
| [List Checklists](actions/list-checklists.md) | `GET /checklist` | [docs](https://developer.hrpartner.io/#get-all-checklists) |
| [List Dependents](actions/list-dependents.md) | `GET /dependents` | [docs](https://developer.hrpartner.io/#dependents) |
| [List Education Records](actions/list-education-records.md) | `GET /education` | [docs](https://developer.hrpartner.io/#education) |
| [List Employee Addresses](actions/list-employee-addresses.md) | `GET /addresses` | [docs](https://developer.hrpartner.io/#employee-addresses) |
| [List Employee Contacts](actions/list-employee-contacts.md) | `GET /contacts` | [docs](https://developer.hrpartner.io/#employee-contacts) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://developer.hrpartner.io/#get-all-employees) |
| [List Expense Claims](actions/list-expense-claims.md) | `GET /expenses` | [docs](https://developer.hrpartner.io/#get-all-expense-claims) |
| [List Goals](actions/list-goals.md) | `GET /goals` | [docs](https://developer.hrpartner.io/#get-all-goals) |
| [List Job Listings](actions/list-job-listings.md) | `GET /jobs` | [docs](https://developer.hrpartner.io/#get-all-job-listings) |
| [List Leave Balances](actions/list-leave-balances.md) | `GET /leave_balances` | [docs](https://developer.hrpartner.io/#get-all-leave-balances) |
| [List Leave Requests](actions/list-leave-requests.md) | `GET /leave_requests` | [docs](https://developer.hrpartner.io/#get-all-leave-requests) |
| [List Library Categories](actions/list-library-categories.md) | `GET /library_categories` | [docs](https://developer.hrpartner.io/#get-library-categories) |
| [List Library Documents](actions/list-library-documents.md) | `GET /library` | [docs](https://developer.hrpartner.io/#get-library-documents) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://developer.hrpartner.io/#notes) |
| [List Performance Reviews](actions/list-performance-reviews.md) | `GET /performances` | [docs](https://developer.hrpartner.io/#get-all-performance-reviews) |
| [List Positions](actions/list-positions.md) | `GET /positions` | [docs](https://developer.hrpartner.io/#positions) |
| [List Reminders](actions/list-reminders.md) | `GET /reminders` | [docs](https://developer.hrpartner.io/#get-all-reminders) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://developer.hrpartner.io/#reviews) |
| [List Skills](actions/list-skills.md) | `GET /skills` | [docs](https://developer.hrpartner.io/#skills) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets` | [docs](https://developer.hrpartner.io/#get-all-timesheets) |
| [List Training Records](actions/list-training-records.md) | `GET /training` | [docs](https://developer.hrpartner.io/#training) |
| [Update Reminder](actions/update-reminder.md) | `POST /reminder/:reminderID` | [docs](https://developer.hrpartner.io/#update-a-reminder) |
