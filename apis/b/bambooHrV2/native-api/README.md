# BambooHR: Native API Reference

A consolidated summary of BambooHR's API configuration and 184 documented operations, with links to official documentation.

- **Official docs:** https://documentation.bamboohr.com/docs
- **API base URL:** `https://{companyDomain}.bamboohr.com/api`

## Authentication

### OAuth2

Connect to your company's BambooHR account with OAuth2 using its Company Subdomain.

### Credentials

- **Company Subdomain:** `companyDomain` · required · Enter only the part before .bamboohr.com. Example: if your address is https://yourcompany.bamboohr.com, enter yourcompany. Do not enter the full address or include .bamboohr.com.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.companyDomain}}.bamboohr.com/authorize.php to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.companyDomain}}.bamboohr.com/token.php.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid offline_access email employee time_off employee:name employee:job payroll benefit`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.companyDomain}}.bamboohr.com/token.php.

[Official authentication documentation](https://documentation.bamboohr.com/docs/getting-started)

### Basic

Use BambooHR API key authentication for BambooHR endpoints that do not support OAuth2. Enter the BambooHR API key; MindCloud will send it as the Basic username and auto-fill the placeholder password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Company Subdomain:** `companyDomain` · required · Enter only the part before .bamboohr.com. Example: if your address is https://yourcompany.bamboohr.com, enter yourcompany. Do not enter the full address or include .bamboohr.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://documentation.bamboohr.com/docs/api-key-permissions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page[limit]` in the query string to set the page size (default 50). Use `page[after]` in the query string as the pagination cursor.

## Endpoints (184 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Time Off Request](actions/add-time-off-request.md) | `PUT /v1/employees/:employeeId/time_off/request` | [docs](https://documentation.bamboohr.com/reference/time-off-add-a-time-off-request) |
| [Change Request Status](actions/change-request-status.md) | `PUT /v1/time_off/requests/:requestId/status` | [docs](https://documentation.bamboohr.com/reference/time-off-change-a-request-status) |
| [Create Employee](actions/create-employee.md) | `POST /v1/employees` | [docs](https://documentation.bamboohr.com/reference/add-employee-2) |
| [Get Alert Configuration](actions/get-alert-configuration.md) | `GET /v1/alert-configurations/:id` | [docs](https://documentation.bamboohr.com/reference/get-alert-configuration) |
| [Get Alignable Goal Options](actions/get-alignable-goal-options.md) | `GET /v1/performance/employees/:employeeId/goals/alignmentOptions` | [docs](https://documentation.bamboohr.com/reference/get-alignable-goal-options) |
| [Get Benefit Coverages](actions/get-benefit-coverages.md) | `GET /v1/benefitcoverages` | [docs](https://documentation.bamboohr.com/reference/get-benefit-coverages-2) |
| [Get Benefit Deduction Types](actions/get-benefit-deduction-types.md) | `GET /v1/benefits/settings/deduction_types/all` | [docs](https://documentation.bamboohr.com/reference/get-benefit-deduction-types-2) |
| [Get Break](actions/get-break.md) | `GET /v1/time-tracking/breaks/:id` | [docs](https://documentation.bamboohr.com/reference/get-break) |
| [Get Break Policy](actions/get-break-policy.md) | `GET /v1/time-tracking/break-policies/:id` | [docs](https://documentation.bamboohr.com/reference/get-break-policy) |
| [Get Catalog Holiday](actions/get-catalog-holiday.md) | `GET /v1/holidays/catalog/:uuid` | [docs](https://documentation.bamboohr.com/reference/get-catalog-holiday) |
| [Get Celebration Template Image Download URL](actions/get-celebration-template-image-download-url.md) | `GET /v1/community/recognition/settings/celebrations/:celebrationType/template-images/:fileId/download-url` | [docs](https://documentation.bamboohr.com/reference/get-celebration-template-image-download-url) |
| [Get Change Communication Letter Details](actions/get-change-communication-letter-details.md) | `GET /v1/compensation/planning_cycles/:id/change_comm` | [docs](https://documentation.bamboohr.com/reference/6c7522fc5664153e97459c2b76ca55ca) |
| [Get Changed Employee I Ds](actions/get-changed-employee-i-ds.md) | `GET /v1/employees/changed` | [docs](https://documentation.bamboohr.com/reference/get-changed-employee-ids) |
| [Get Changed Employee Table Data](actions/get-changed-employee-table-data.md) | `GET /v1/employees/changed/tables/:table` | [docs](https://documentation.bamboohr.com/reference/get-changed-employee-table-data) |
| [Get Changed Employees](actions/get-changed-employees.md) | `GET /v1/employees/changed/[:type]` | [docs](https://documentation.bamboohr.com/reference/changed-employee-ids) |
| [Get Clock Entry](actions/get-clock-entry.md) | `GET /v1/time-tracking/clock-entries/:id` | [docs](https://documentation.bamboohr.com/reference/get-clock-entry) |
| [Get Company Benefits](actions/get-company-benefits.md) | `GET /v1/benefit/company_benefit` | [docs](https://documentation.bamboohr.com/reference/get-company-benefits-1) |
| [Get Company Equity Settings](actions/get-company-equity-settings.md) | `GET /v1/compensation/equity/settings` | [docs](https://documentation.bamboohr.com/reference/d90d59c4f1201ea05c23a1313c071db4) |
| [Get Company File](actions/get-company-file.md) | `GET /v1/files/:fileId` | [docs](https://documentation.bamboohr.com/reference/get-company-file) |
| [Get Company Holiday](actions/get-company-holiday.md) | `GET /v1/holidays/:id` | [docs](https://documentation.bamboohr.com/reference/get-company-holiday) |
| [Get Company Information](actions/get-company-information.md) | `GET /v1/company_information` | [docs](https://documentation.bamboohr.com/reference/get-company-information-1) |
| [Get Company Profile Integrations](actions/get-company-profile-integrations.md) | `GET /v1/company-profile-integrations` | [docs](https://documentation.bamboohr.com/reference/get-company-profile-integrations) |
| [Get Company Properties](actions/get-company-properties.md) | `GET /v1/meta/company` | [docs](https://documentation.bamboohr.com/reference/get-meta-company) |
| [Get Compensation Benchmark Details](actions/get-compensation-benchmark-details.md) | `GET /v1/compensation/benchmarks/details` | [docs](https://documentation.bamboohr.com/reference/get-compensation-benchmark-details) |
| [Get Compensation Benchmark Export](actions/get-compensation-benchmark-export.md) | `GET /v1/compensation/benchmarks/details/export` | [docs](https://documentation.bamboohr.com/reference/export-compensation-benchmark-details) |
| [Get Compensation Level Group Status Counts](actions/get-compensation-level-group-status-counts.md) | `GET /v1/pay-grades-and-bands/status-counts` | [docs](https://documentation.bamboohr.com/reference/get-compensation-level-group-status-counts) |
| [Get Compensation Planning Approval Flows](actions/get-compensation-planning-approval-flows.md) | `GET /v1/compensation/planning_cycles/:id/approvals` | [docs](https://documentation.bamboohr.com/reference/552aef08bdce5fca9ed705bfdcb945b5) |
| [Get Compensation Planning Cycle Budgets](actions/get-compensation-planning-cycle-budgets.md) | `GET /v1/compensation/planning_cycles/:id/budgets` | [docs](https://documentation.bamboohr.com/reference/bdb215e3f9e84ed281eb797b48cc66cc) |
| [Get Compensation Planning Cycle Details](actions/get-compensation-planning-cycle-details.md) | `GET /v1/compensation/planning_cycles/:id` | [docs](https://documentation.bamboohr.com/reference/342202015a4b67f43d3b993707f544c1) |
| [Get Compensation Planning Cycle Summary](actions/get-compensation-planning-cycle-summary.md) | `GET /v1/compensation/planning_cycles/:id/summary` | [docs](https://documentation.bamboohr.com/reference/d1668054a24382361803d12c3ee41669) |
| [Get Compensation Planning Cycle Worksheet](actions/get-compensation-planning-cycle-worksheet.md) | `GET /v1/compensation/planning_cycles/:id/worksheet` | [docs](https://documentation.bamboohr.com/reference/fdffbb9803f77a9bd0c13a3f206a41d4) |
| [Get Compensation Planning Worksheet CSV](actions/get-compensation-planning-worksheet-csv.md) | `GET /v1/compensation/planning_cycles/:id/worksheet/export` | [docs](https://documentation.bamboohr.com/reference/f4ccbeaf25b2344e5026de3c8189dd5e) |
| [Get Country by ID](actions/get-country-by-id.md) | `GET /v1/meta/countries/:id` | [docs](https://documentation.bamboohr.com/reference/get-country-by-id) |
| [Get Currency Conversion Rates](actions/get-currency-conversion-rates.md) | `GET /v1/meta/currency-conversions` | [docs](https://documentation.bamboohr.com/reference/get-currency-conversions) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /v1/hris/custom-fields/:customFieldId` | [docs](https://documentation.bamboohr.com/reference/get-custom-field) |
| [Get Custom Table](actions/get-custom-table.md) | `GET /v1/hris/custom-tables/:customTableId` | [docs](https://documentation.bamboohr.com/reference/get-custom-table) |
| [Get Datasets](actions/get-datasets.md) | `GET /v1/datasets` | [docs](https://documentation.bamboohr.com/reference/get-datasets) |
| [Get Employee](actions/get-employee.md) | `GET /v1/employees/:id` | [docs](https://documentation.bamboohr.com/reference/get-employee-1) |
| [Get Employee Benefits](actions/get-employee-benefits.md) | `GET /v1/benefit/employee_benefit` | [docs](https://documentation.bamboohr.com/reference/get-employee-benefit-1) |
| [Get Employee Dependent](actions/get-employee-dependent.md) | `GET /v1/employeedependents/:id` | [docs](https://documentation.bamboohr.com/reference/get-employee-dependent-2) |
| [Get Employee Dependents](actions/get-employee-dependents.md) | `GET /v1/employeedependents` | [docs](https://documentation.bamboohr.com/reference/get-employee-dependents-2) |
| [Get Employee Directory](actions/get-employee-directory.md) | `GET /v1/employees/directory` | [docs](https://documentation.bamboohr.com/reference/get-employees-directory) |
| [Get Employee Enrollment](actions/get-employee-enrollment.md) | `GET /v1/time-tracking/employees/:employeeId` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-employee-enrollment) |
| [Get Employee File](actions/get-employee-file.md) | `GET /v1/employees/:id/files/:fileId` | [docs](https://documentation.bamboohr.com/reference/get-employee-file) |
| [Get Employee Onboarding Experience by ID](actions/get-employee-onboarding-experience-by-id.md) | `GET /v1/employees/:employeeId/onboarding-experiences/:onboardingExperienceId` | [docs](https://documentation.bamboohr.com/reference/180314d815c8b991c1e07c8e32851639) |
| [Get Employee Photo](actions/get-employee-photo.md) | `GET /v1/employees/:employeeId/photo/:size` | [docs](https://documentation.bamboohr.com/reference/get-employee-photo) |
| [Get Employee Verification Integration Status](actions/get-employee-verification-integration-status.md) | `GET /v1/employee-verifications/integration` | [docs](https://documentation.bamboohr.com/reference/get-employee-verification-integration) |
| [Get Fields](actions/get-fields.md) | `GET /v1/meta/fields` | [docs](https://documentation.bamboohr.com/reference/metadata-get-a-list-of-fields-1) |
| [Get Fields from Dataset](actions/get-fields-from-dataset.md) | `GET /v1/datasets/:datasetName/fields` | [docs](https://documentation.bamboohr.com/reference/get-fields-from-dataset-2) |
| [Get Fields from Dataset V1 2](actions/get-fields-from-dataset-v12.md) | `GET /v1_2/datasets/:datasetName/fields` | [docs](https://documentation.bamboohr.com/reference/get-fields-from-dataset-v1_2) |
| [Get Goal Aggregate](actions/get-goal-aggregate.md) | `GET /v1/performance/employees/:employeeId/goals/:goalId/aggregate` | [docs](https://documentation.bamboohr.com/reference/get-goal-aggregate) |
| [Get Goal Creation Permission](actions/get-goal-creation-permission.md) | `GET /v1/performance/employees/:employeeId/goals/canCreateGoals` | [docs](https://documentation.bamboohr.com/reference/get-goal-creation-permission) |
| [Get Goal Filters V1 2](actions/get-goal-filters-v12.md) | `GET /v1_2/performance/employees/:employeeId/goals/filters` | [docs](https://documentation.bamboohr.com/reference/get-goals-filters-v1_2) |
| [Get Goals Aggregate V1 2](actions/get-goals-aggregate-v12.md) | `GET /v1_2/performance/employees/:employeeId/goals/aggregate` | [docs](https://documentation.bamboohr.com/reference/get-goals-aggregate-v1_2) |
| [Get Hour Entry](actions/get-hour-entry.md) | `GET /v1/time-tracking/hour-entries/:id` | [docs](https://documentation.bamboohr.com/reference/get-hour-entry) |
| [Get Job Application Details](actions/get-job-application-details.md) | `GET /v1/applicant_tracking/applications/:applicationId` | [docs](https://documentation.bamboohr.com/reference/get-application-details) |
| [Get Job Location](actions/get-job-location.md) | `GET /v1/hris/org/locations/:id` | [docs](https://documentation.bamboohr.com/reference/get-location) |
| [Get Job Titles and Level Assignments](actions/get-job-titles-and-level-assignments.md) | `GET /v1/pay-grades-and-bands/job-titles` | [docs](https://documentation.bamboohr.com/reference/get-job-title-level-assignments) |
| [Get Legacy Report Field Map](actions/get-legacy-report-field-map.md) | `GET /v1/custom-reports/legacy-field-map` | [docs](https://documentation.bamboohr.com/reference/get-legacy-report-field-map) |
| [Get Legacy Report ID Map](actions/get-legacy-report-id-map.md) | `GET /v1/custom-reports/legacy-id-map` | [docs](https://documentation.bamboohr.com/reference/get-legacy-report-id-map) |
| [Get Levels and Bands Review](actions/get-levels-and-bands-review.md) | `GET /v1/pay-grades-and-bands/review` | [docs](https://documentation.bamboohr.com/reference/get-levels-and-bands-review) |
| [Get Levels and Bands Status](actions/get-levels-and-bands-status.md) | `GET /v1/pay-grades-and-bands/status` | [docs](https://documentation.bamboohr.com/reference/get-levels-and-bands-status) |
| [Get List Field Details](actions/get-list-field-details.md) | `GET /v1/meta/lists` | [docs](https://documentation.bamboohr.com/reference/metadata-get-details-for-list-fields) |
| [Get Member Benefit Events](actions/get-member-benefit-events.md) | `GET /v1/benefit/member_benefit` | [docs](https://documentation.bamboohr.com/reference/get-member-benefit-2) |
| [Get Member Benefits](actions/get-member-benefits.md) | `GET /v1/benefits/member-benefits` | [docs](https://documentation.bamboohr.com/reference/get-member-benefits) |
| [Get New Hire Packet by ID](actions/get-new-hire-packet-by-id.md) | `GET /v1/new-hire-packets/:id` | [docs](https://documentation.bamboohr.com/reference/9e50205e7d1577fae12f069776d705f7) |
| [Get Pay Bands](actions/get-pay-bands.md) | `GET /v1/pay-grades-and-bands/pay-bands` | [docs](https://documentation.bamboohr.com/reference/get-pay-bands) |
| [Get Printable Total Rewards Statement](actions/get-printable-total-rewards-statement.md) | `GET /v1/compensation/total_rewards/:employeeId/printable` | [docs](https://documentation.bamboohr.com/reference/get-total-rewards-printable-statement) |
| [Get Published Levels and Bands](actions/get-published-levels-and-bands.md) | `GET /v1/pay-grades-and-bands` | [docs](https://documentation.bamboohr.com/reference/get-published-levels-and-bands) |
| [Get Report by ID](actions/get-report-by-id.md) | `GET /v1/custom-reports/:reportId` | [docs](https://documentation.bamboohr.com/reference/getbyreportid-2) |
| [Get Reports](actions/get-reports.md) | `GET /v1/custom-reports` | [docs](https://documentation.bamboohr.com/reference/custom-reports-1) |
| [Get Schedule](actions/get-schedule.md) | `GET /v1/scheduling/schedules/:id` | [docs](https://documentation.bamboohr.com/reference/scheduling-get-schedule) |
| [Get Schedule PDF](actions/get-schedule-pdf.md) | `GET /v1/scheduling/schedules/:id/pdf` | [docs](https://documentation.bamboohr.com/reference/scheduling-get-schedule-pdf) |
| [Get Shift](actions/get-shift.md) | `GET /v1/scheduling/shifts/:id` | [docs](https://documentation.bamboohr.com/reference/scheduling-get-shift) |
| [Get Tabular Fields](actions/get-tabular-fields.md) | `GET /v1/meta/tables` | [docs](https://documentation.bamboohr.com/reference/metadata-get-a-list-of-tabular-fields) |
| [Get Time Off Balance](actions/get-time-off-balance.md) | `GET /v1/employees/:employeeId/time_off/calculator` | [docs](https://documentation.bamboohr.com/reference/time-off-get-time-off-balance) |
| [Get Time Off Category](actions/get-time-off-category.md) | `GET /v1/time-off/categories/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-off-category) |
| [Get Time Off Policies](actions/get-time-off-policies.md) | `GET /v1/meta/time_off/policies` | [docs](https://documentation.bamboohr.com/reference/get-time-off-policies-1) |
| [Get Time Off Policies for Employee](actions/get-time-off-policies-for-employee.md) | `GET /v1/employees/:employeeId/time_off/policies` | [docs](https://documentation.bamboohr.com/reference/time-off-list-time-off-policies-for-employee-1) |
| [Get Time Off Policy](actions/get-time-off-policy.md) | `GET /v1/time-off/policies/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-off-policy) |
| [Get Time Off Request](actions/get-time-off-request.md) | `GET /v1/time-off/requests/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-off-request) |
| [Get Time Off Requests](actions/get-time-off-requests.md) | `GET /v1/time_off/requests` | [docs](https://documentation.bamboohr.com/reference/time-off-get-time-off-requests) |
| [Get Time Off Types](actions/get-time-off-types.md) | `GET /v1/meta/time_off/types` | [docs](https://documentation.bamboohr.com/reference/get-time-off-types-1) |
| [Get Time Tracking Configuration](actions/get-time-tracking-configuration.md) | `GET /v1/time-tracking/configurations/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-configuration) |
| [Get Time Tracking Import](actions/get-time-tracking-import.md) | `GET /v1/time-tracking/imports/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-import) |
| [Get Time Tracking Import Row](actions/get-time-tracking-import-row.md) | `GET /v1/time-tracking/imports/:id/rows/:rowId` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-import-row) |
| [Get Time Tracking Kiosk](actions/get-time-tracking-kiosk.md) | `GET /v1/time-tracking/kiosks/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-kiosk) |
| [Get Time Tracking Project](actions/get-time-tracking-project.md) | `GET /v1/time-tracking/projects/:id` | [docs](https://documentation.bamboohr.com/reference/get-project) |
| [Get Time Tracking Record](actions/get-time-tracking-record.md) | `GET /v1/timetracking/record/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-record) |
| [Get Time Tracking Shift Differential](actions/get-time-tracking-shift-differential.md) | `GET /v1/time-tracking/shift-differentials/:id` | [docs](https://documentation.bamboohr.com/reference/get-shift-differential) |
| [Get Time Tracking Task](actions/get-time-tracking-task.md) | `GET /v1/time-tracking/tasks/:id` | [docs](https://documentation.bamboohr.com/reference/get-task) |
| [Get Time Tracking Time Clock](actions/get-time-tracking-time-clock.md) | `GET /v1/time-tracking/time-clocks/:id` | [docs](https://documentation.bamboohr.com/reference/get-time-tracking-time-clock) |
| [Get Timesheet](actions/get-timesheet.md) | `GET /v1/time-tracking/timesheets/:id` | [docs](https://documentation.bamboohr.com/reference/get-timesheet) |
| [Get Timesheet Summary](actions/get-timesheet-summary.md) | `GET /v1/time-tracking/timesheets/:id/summary` | [docs](https://documentation.bamboohr.com/reference/get-timesheet-summary) |
| [Get Timezone by ID](actions/get-timezone-by-id.md) | `GET /v1/meta/timezones/:id` | [docs](https://documentation.bamboohr.com/reference/baa7162824294d030115568d1d8e6ca7) |
| [Get Timezone by ZIP Code](actions/get-timezone-by-zip-code.md) | `GET /v1/meta/timezones/by-zip/:zip` | [docs](https://documentation.bamboohr.com/reference/10d66d8561dd7dac50ff9c21ef63d83b) |
| [Get Total Rewards Profile Availability](actions/get-total-rewards-profile-availability.md) | `GET /v1/compensation/total_rewards/:employeeId` | [docs](https://documentation.bamboohr.com/reference/check-total-rewards-profile) |
| [Get Total Rewards Statement](actions/get-total-rewards-statement.md) | `GET /v1/compensation/total_rewards/:employeeId/statement` | [docs](https://documentation.bamboohr.com/reference/get-total-rewards-statement) |
| [Get Users](actions/get-users.md) | `GET /v1/meta/users` | [docs](https://documentation.bamboohr.com/reference/get-list-of-users-1) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:id` | [docs](https://documentation.bamboohr.com/reference/get-webhook) |
| [Get Welcome New Hires Widget](actions/get-welcome-new-hires-widget.md) | `GET /v1/onboarding/new-hire-widget` | [docs](https://documentation.bamboohr.com/reference/b5c0155d30e7dc52aabacf0a2db87e48) |
| [Get Who's Out](actions/get-whos-out.md) | `GET /v1/time_off/whos_out` | [docs](https://documentation.bamboohr.com/reference/get-a-list-of-who-is-out-1) |
| [List Absent Employees](actions/list-absent-employees.md) | `GET /v1/whos-out` | [docs](https://documentation.bamboohr.com/reference/list-whos-out-v1) |
| [List Alert Configurations](actions/list-alert-configurations.md) | `GET /v1/alert-configurations` | [docs](https://documentation.bamboohr.com/reference/list-alert-configurations) |
| [List Alert Templates](actions/list-alert-templates.md) | `GET /v1/alerts` | [docs](https://documentation.bamboohr.com/reference/list-alert-templates) |
| [List Applicant Statuses](actions/list-applicant-statuses.md) | `GET /v1/applicant_tracking/statuses` | [docs](https://documentation.bamboohr.com/reference/get-statuses) |
| [List Archived Custom Fields](actions/list-archived-custom-fields.md) | `GET /v1/hris/custom-fields/archived` | [docs](https://documentation.bamboohr.com/reference/list-archived-custom-fields) |
| [List Available Compensation Tools](actions/list-available-compensation-tools.md) | `GET /v1/compensation/tools` | [docs](https://documentation.bamboohr.com/reference/e7d3012f6a8f037cb74486bcf3a77bde) |
| [List Bank Holidays](actions/list-bank-holidays.md) | `GET /v1/meta/bank-holidays` | [docs](https://documentation.bamboohr.com/reference/list-bank-holidays) |
| [List Break Assessments](actions/list-break-assessments.md) | `GET /v1/time-tracking/break-assessments` | [docs](https://documentation.bamboohr.com/reference/list-break-assessments) |
| [List Break Policies](actions/list-break-policies.md) | `GET /v1/time-tracking/break-policies` | [docs](https://documentation.bamboohr.com/reference/list-break-policies) |
| [List Break Policy Employees](actions/list-break-policy-employees.md) | `GET /v1/time-tracking/break-policies/:id/employees` | [docs](https://documentation.bamboohr.com/reference/list-break-policy-employees) |
| [List Breaks for Break Policy](actions/list-breaks-for-break-policy.md) | `GET /v1/time-tracking/break-policies/:id/breaks` | [docs](https://documentation.bamboohr.com/reference/list-break-policy-breaks) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /v1/calendar-events` | [docs](https://documentation.bamboohr.com/reference/list-calendar-events) |
| [List Catalog Holidays](actions/list-catalog-holidays.md) | `GET /v1/holidays/catalog` | [docs](https://documentation.bamboohr.com/reference/list-catalog-holidays) |
| [List Clock Entries](actions/list-clock-entries.md) | `GET /v1/time-tracking/clock-entries` | [docs](https://documentation.bamboohr.com/reference/list-clock-entries) |
| [List Company Files and Categories](actions/list-company-files-and-categories.md) | `GET /v1/files/view` | [docs](https://documentation.bamboohr.com/reference/list-company-files) |
| [List Company Holidays](actions/list-company-holidays.md) | `GET /v1/holidays` | [docs](https://documentation.bamboohr.com/reference/list-company-holidays) |
| [List Compensation Benchmark Sources](actions/list-compensation-benchmark-sources.md) | `GET /v1/compensation/benchmarks/sources` | [docs](https://documentation.bamboohr.com/reference/list-compensation-benchmark-sources) |
| [List Compensation Benchmarks](actions/list-compensation-benchmarks.md) | `GET /v1/compensation/benchmarks` | [docs](https://documentation.bamboohr.com/reference/list-compensation-benchmarks) |
| [List Compensation Level Groups and Levels](actions/list-compensation-level-groups-and-levels.md) | `GET /v1/pay-grades-and-bands/levels` | [docs](https://documentation.bamboohr.com/reference/list-compensation-level-groups-and-levels) |
| [List Compensation Planning Cycle Admins](actions/list-compensation-planning-cycle-admins.md) | `GET /v1/compensation/planning_cycles/:id/admins` | [docs](https://documentation.bamboohr.com/reference/8033792a7b9b696a22d0bd19ff09b1df) |
| [List Compensation Planning Cycles](actions/list-compensation-planning-cycles.md) | `GET /v1/compensation/planning_cycles` | [docs](https://documentation.bamboohr.com/reference/186eb76d2c656f8309cae9dff6ed8a69) |
| [List Countries](actions/list-countries.md) | `GET /v1/meta/countries/options` | [docs](https://documentation.bamboohr.com/reference/get-countries-options) |
| [List Country Provinces](actions/list-country-provinces.md) | `GET /v1/meta/provinces/:countryId` | [docs](https://documentation.bamboohr.com/reference/get-states-by-country-id) |
| [List Currency Types](actions/list-currency-types.md) | `GET /v1/meta/currency/types` | [docs](https://documentation.bamboohr.com/reference/get-all-currency-types) |
| [List Custom Field List Values](actions/list-custom-field-list-values.md) | `GET /v1/hris/custom-fields/:customFieldId/list-values` | [docs](https://documentation.bamboohr.com/reference/list-custom-field-list-values) |
| [List Custom Field Types](actions/list-custom-field-types.md) | `GET /v1/hris/custom-fields/types` | [docs](https://documentation.bamboohr.com/reference/list-custom-field-types) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /v1/hris/custom-fields` | [docs](https://documentation.bamboohr.com/reference/list-custom-fields) |
| [List Custom Tables](actions/list-custom-tables.md) | `GET /v1/hris/custom-tables` | [docs](https://documentation.bamboohr.com/reference/list-custom-tables) |
| [List Datasets V1 2](actions/list-datasets-v12.md) | `GET /v1_2/datasets` | [docs](https://documentation.bamboohr.com/reference/list-datasets-v1_2) |
| [List Employee Break Availabilities](actions/list-employee-break-availabilities.md) | `GET /v1/time-tracking/employees/:id/break-availabilities` | [docs](https://documentation.bamboohr.com/reference/list-employee-break-availabilities) |
| [List Employee Break Policies](actions/list-employee-break-policies.md) | `GET /v1/time-tracking/employees/:id/break-policies` | [docs](https://documentation.bamboohr.com/reference/list-employee-break-policies) |
| [List Employee Files](actions/list-employee-files.md) | `GET /v1/employees/:id/files/view` | [docs](https://documentation.bamboohr.com/reference/list-employee-files) |
| [List Employee Onboarding Experiences](actions/list-employee-onboarding-experiences.md) | `GET /v1/employees/:employeeId/onboarding-experiences` | [docs](https://documentation.bamboohr.com/reference/b678783b410374647b30c1e034d24f69) |
| [List Employee Table Rows](actions/list-employee-table-rows.md) | `GET /v1/employees/:id/tables/:table` | [docs](https://documentation.bamboohr.com/reference/get-employee-table-data) |
| [List Employee Time Off Policies](actions/list-employee-time-off-policies.md) | `GET /v1/employees/:employeeId/time-off/policies` | [docs](https://documentation.bamboohr.com/reference/list-employee-time-off-policies) |
| [List Employee Time Off Policies V1 1](actions/list-employee-time-off-policies-v11.md) | `GET /v1_1/employees/:employeeId/time_off/policies` | [docs](https://documentation.bamboohr.com/reference/list-employee-time-off-policies-v1_1) |
| [List Employee Training Records](actions/list-employee-training-records.md) | `GET /v1/training/record/employee/:employeeId` | [docs](https://documentation.bamboohr.com/reference/list-employee-trainings) |
| [List Employee Verification Records for an Employee](actions/list-employee-verification-records-for-an-employee.md) | `GET /v1/employee-verifications/employees/:employeeId` | [docs](https://documentation.bamboohr.com/reference/list-employee-verifications-by-employee) |
| [List Employees](actions/list-employees.md) | `GET /v1/employees` | [docs](https://documentation.bamboohr.com/reference/get-employees-list) |
| [List Employees in Compensation Planning Cycle](actions/list-employees-in-compensation-planning-cycle.md) | `GET /v1/compensation/planning_cycles/:id/employees` | [docs](https://documentation.bamboohr.com/reference/7ef1060e521f3ca40c83235180b8654c) |
| [List Enrolled Employees](actions/list-enrolled-employees.md) | `GET /v1/time-tracking/employees` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-employees) |
| [List Goal Comments](actions/list-goal-comments.md) | `GET /v1/performance/employees/:employeeId/goals/:goalId/comments` | [docs](https://documentation.bamboohr.com/reference/list-goal-comments) |
| [List Goal Sharing Options](actions/list-goal-sharing-options.md) | `GET /v1/performance/employees/:employeeId/goals/shareOptions` | [docs](https://documentation.bamboohr.com/reference/list-goal-share-options) |
| [List Goals](actions/list-goals.md) | `GET /v1/performance/employees/:employeeId/goals` | [docs](https://documentation.bamboohr.com/reference/list-goals) |
| [List Hiring Leads](actions/list-hiring-leads.md) | `GET /v1/applicant_tracking/hiring_leads` | [docs](https://documentation.bamboohr.com/reference/get-hiring-leads) |
| [List Hiring Locations](actions/list-hiring-locations.md) | `GET /v1/applicant_tracking/locations` | [docs](https://documentation.bamboohr.com/reference/get-company-locations) |
| [List Hour Entries](actions/list-hour-entries.md) | `GET /v1/time-tracking/hour-entries` | [docs](https://documentation.bamboohr.com/reference/list-hour-entries) |
| [List Industries](actions/list-industries.md) | `GET /v1/meta/industries` | [docs](https://documentation.bamboohr.com/reference/list-industries) |
| [List Job Applications](actions/list-job-applications.md) | `GET /v1/applicant_tracking/applications` | [docs](https://documentation.bamboohr.com/reference/get-applications) |
| [List Job Locations](actions/list-job-locations.md) | `GET /v1/hris/org/locations` | [docs](https://documentation.bamboohr.com/reference/get-locations) |
| [List Job Summaries](actions/list-job-summaries.md) | `GET /v1/applicant_tracking/jobs` | [docs](https://documentation.bamboohr.com/reference/get-job-summaries) |
| [List Job Titles with Employees](actions/list-job-titles-with-employees.md) | `GET /v1/pay-grades-and-bands/job-titles-with-employees` | [docs](https://documentation.bamboohr.com/reference/list-job-titles-with-employees) |
| [List Monitor Fields](actions/list-monitor-fields.md) | `GET /v1/webhooks/monitor_fields` | [docs](https://documentation.bamboohr.com/reference/list-monitor-fields) |
| [List New Hire Packets](actions/list-new-hire-packets.md) | `GET /v1/new-hire-packets` | [docs](https://documentation.bamboohr.com/reference/6d181e2defa79e054c4415c11dc42dab) |
| [List Open Shifts](actions/list-open-shifts.md) | `GET /v1/scheduling/open-shifts` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-open-shifts) |
| [List Provinces](actions/list-provinces.md) | `GET /v1/meta/provinces` | [docs](https://documentation.bamboohr.com/reference/get-all-provinces) |
| [List Schedules](actions/list-schedules.md) | `GET /v1/scheduling/schedules` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-schedules) |
| [List Scheduling Timezones](actions/list-scheduling-timezones.md) | `GET /v1/scheduling/timezones` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-timezones) |
| [List Shift Assessments](actions/list-shift-assessments.md) | `GET /v1/scheduling/shift-assessments` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-shift-assessments) |
| [List Shift Claims](actions/list-shift-claims.md) | `GET /v1/scheduling/shift-claims` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-shift-claims) |
| [List Shifts](actions/list-shifts.md) | `GET /v1/scheduling/shifts` | [docs](https://documentation.bamboohr.com/reference/scheduling-list-shifts) |
| [List Time Off Policies](actions/list-time-off-policies.md) | `GET /v1/time-off/policies` | [docs](https://documentation.bamboohr.com/reference/list-time-off-policies-v1) |
| [List Time Off Policy Versions](actions/list-time-off-policy-versions.md) | `GET /v1/time-off/policies/:id/versions` | [docs](https://documentation.bamboohr.com/reference/list-time-off-policy-versions) |
| [List Time Off Request Comments](actions/list-time-off-request-comments.md) | `GET /v1/time-off/requests/:id/comments` | [docs](https://documentation.bamboohr.com/reference/list-time-off-request-comments) |
| [List Time Off Requests](actions/list-time-off-requests.md) | `GET /v1/time-off/requests` | [docs](https://documentation.bamboohr.com/reference/list-time-off-requests-v1) |
| [List Time Tracking Configurations](actions/list-time-tracking-configurations.md) | `GET /v1/time-tracking/configurations` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-configurations) |
| [List Time Tracking Import Rows](actions/list-time-tracking-import-rows.md) | `GET /v1/time-tracking/imports/:id/rows` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-import-rows) |
| [List Time Tracking Imports](actions/list-time-tracking-imports.md) | `GET /v1/time-tracking/imports` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-imports) |
| [List Time Tracking Kiosks](actions/list-time-tracking-kiosks.md) | `GET /v1/time-tracking/kiosks` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-kiosks) |
| [List Time Tracking Project Tasks](actions/list-time-tracking-project-tasks.md) | `GET /v1/time-tracking/projects/:projectId/tasks` | [docs](https://documentation.bamboohr.com/reference/list-project-tasks) |
| [List Time Tracking Projects](actions/list-time-tracking-projects.md) | `GET /v1/time-tracking/projects` | [docs](https://documentation.bamboohr.com/reference/list-projects) |
| [List Time Tracking Shift Differentials](actions/list-time-tracking-shift-differentials.md) | `GET /v1/time-tracking/shift-differentials` | [docs](https://documentation.bamboohr.com/reference/list-shift-differentials) |
| [List Time Tracking Time Clocks](actions/list-time-tracking-time-clocks.md) | `GET /v1/time-tracking/time-clocks` | [docs](https://documentation.bamboohr.com/reference/list-time-tracking-time-clocks) |
| [List Timesheet Entries](actions/list-timesheet-entries.md) | `GET /v1/time_tracking/timesheet_entries` | [docs](https://documentation.bamboohr.com/reference/list-timesheet-entries) |
| [List Timesheets](actions/list-timesheets.md) | `GET /v1/time-tracking/timesheets` | [docs](https://documentation.bamboohr.com/reference/list-timesheets) |
| [List Timezones](actions/list-timezones.md) | `GET /v1/meta/timezones` | [docs](https://documentation.bamboohr.com/reference/5c5fb0f1211ae1c9451753f92f1053b6) |
| [List Training Categories](actions/list-training-categories.md) | `GET /v1/training/category` | [docs](https://documentation.bamboohr.com/reference/list-training-categories) |
| [List Training Types](actions/list-training-types.md) | `GET /v1/training/type` | [docs](https://documentation.bamboohr.com/reference/list-training-types) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `GET /v1/webhooks/:id/log` | [docs](https://documentation.bamboohr.com/reference/list-webhook-logs) |
| [List Webhook Post Fields](actions/list-webhook-post-fields.md) | `GET /v1/webhooks/post-fields` | [docs](https://documentation.bamboohr.com/reference/get-post-fields) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://documentation.bamboohr.com/reference/list-webhooks) |
| [Update Employee](actions/update-employee.md) | `POST /v1/employees/:employeeId` | [docs](https://documentation.bamboohr.com/reference/update-employee-1) |
