# <img src="https://images.mindcloud.co/apps/icons/bamboo-hr_1773069235672.png" alt="BambooHR logo" width="28" height="28"> BambooHR: Universal API

Manage employee records, time off, benefits, and directory data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bambooHrV2/latest
- **Category:** Human Resources / HRIS
- **Actions:** 184
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bamboohr.com
- **Vendor API docs:** https://documentation.bamboohr.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (184)

### Account Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Properties](actions/get-company-properties.md) | GET | Retrieves company properties from BambooHR. |
| [Get Country by ID](actions/get-country-by-id.md) | GET | Retrieves country by id from BambooHR. |
| [Get Currency Conversion Rates](actions/get-currency-conversion-rates.md) | GET | Retrieves currency conversion rates from BambooHR. |
| [Get Timezone by ID](actions/get-timezone-by-id.md) | GET | Retrieves timezone by id from BambooHR. |
| [Get Timezone by ZIP Code](actions/get-timezone-by-zip-code.md) | GET | Retrieves timezone by zip code from BambooHR. |
| [List Bank Holidays](actions/list-bank-holidays.md) | GET | Lists bank holidays from BambooHR. |
| [List Countries](actions/list-countries.md) | GET | Lists countries from BambooHR. |
| [List Country Provinces](actions/list-country-provinces.md) | GET | Lists country provinces from BambooHR. |
| [List Currency Types](actions/list-currency-types.md) | GET | Lists currency types from BambooHR. |
| [List Industries](actions/list-industries.md) | GET | Lists industries from BambooHR. |
| [List Provinces](actions/list-provinces.md) | GET | Lists provinces from BambooHR. |
| [List Timezones](actions/list-timezones.md) | GET | Lists timezones from BambooHR. |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Configuration](actions/get-alert-configuration.md) | GET | Retrieves alert configuration from BambooHR. |
| [List Alert Configurations](actions/list-alert-configurations.md) | GET | Lists alert configurations from BambooHR. |
| [List Alert Templates](actions/list-alert-templates.md) | GET | Lists alert templates from BambooHR. |

### Applicant Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Application Details](actions/get-job-application-details.md) | GET | Retrieves job application details from BambooHR. |
| [List Applicant Statuses](actions/list-applicant-statuses.md) | GET | Lists applicant statuses from BambooHR. |
| [List Hiring Leads](actions/list-hiring-leads.md) | GET | Lists hiring leads from BambooHR. |
| [List Hiring Locations](actions/list-hiring-locations.md) | GET | Lists hiring locations from BambooHR. |
| [List Job Applications](actions/list-job-applications.md) | GET | Lists job applications from BambooHR. |
| [List Job Summaries](actions/list-job-summaries.md) | GET | Lists job summaries from BambooHR. |

### Benefits

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Benefits](actions/get-employee-benefits.md) | GET | Retrieves employee benefit enrollments from BambooHR. |
| [Get Member Benefit Events](actions/get-member-benefit-events.md) | GET | Retrieves member benefit events from BambooHR. |
| [Get Member Benefits](actions/get-member-benefits.md) | GET | Retrieves member benefit enrollments from BambooHR. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Lists calendar events from BambooHR. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Benefit Coverages](actions/get-benefit-coverages.md) | GET | Retrieves benefit coverage options from BambooHR. |
| [Get Benefit Deduction Types](actions/get-benefit-deduction-types.md) | GET | Retrieves benefit deduction types from BambooHR. |
| [Get Time Off Types](actions/get-time-off-types.md) | GET | Retrieves time off types from BambooHR. |

### Change Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Changed Employee I Ds](actions/get-changed-employee-i-ds.md) | GET | Retrieves changed employee i ds from BambooHR. |
| [Get Changed Employee Table Data](actions/get-changed-employee-table-data.md) | GET | Retrieves changed employee table data from BambooHR. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Information](actions/get-company-information.md) | GET | Retrieves company profile information from BambooHR. |

### Company Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Company File](actions/get-company-file.md) | GET | Retrieves company file from BambooHR. |
| [List Company Files and Categories](actions/list-company-files-and-categories.md) | GET | Lists company files and categories from BambooHR. |

### Company Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Profile Integrations](actions/get-company-profile-integrations.md) | GET | Retrieves company profile integrations from BambooHR. |

### Compensation

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Equity Settings](actions/get-company-equity-settings.md) | GET | Retrieves company equity settings from BambooHR. |
| [List Available Compensation Tools](actions/list-available-compensation-tools.md) | GET | Lists available compensation tools from BambooHR. |

### Compensation Benchmarking

| Action | Method | Description |
| --- | --- | --- |
| [Get Compensation Benchmark Details](actions/get-compensation-benchmark-details.md) | GET | Retrieves compensation benchmark details from BambooHR. |
| [Get Compensation Benchmark Export](actions/get-compensation-benchmark-export.md) | GET | Retrieves compensation benchmark export from BambooHR. |
| [List Compensation Benchmark Sources](actions/list-compensation-benchmark-sources.md) | GET | Lists compensation benchmark sources from BambooHR. |
| [List Compensation Benchmarks](actions/list-compensation-benchmarks.md) | GET | Lists compensation benchmarks from BambooHR. |

### Compensation Planning

| Action | Method | Description |
| --- | --- | --- |
| [Get Change Communication Letter Details](actions/get-change-communication-letter-details.md) | GET | Retrieves change communication letter details from BambooHR. |
| [Get Compensation Planning Approval Flows](actions/get-compensation-planning-approval-flows.md) | GET | Retrieves compensation planning approval flows from BambooHR. |
| [Get Compensation Planning Cycle Budgets](actions/get-compensation-planning-cycle-budgets.md) | GET | Retrieves compensation planning cycle budgets from BambooHR. |
| [Get Compensation Planning Cycle Details](actions/get-compensation-planning-cycle-details.md) | GET | Retrieves compensation planning cycle details from BambooHR. |
| [Get Compensation Planning Cycle Summary](actions/get-compensation-planning-cycle-summary.md) | GET | Retrieves compensation planning cycle summary from BambooHR. |
| [Get Compensation Planning Cycle Worksheet](actions/get-compensation-planning-cycle-worksheet.md) | GET | Retrieves compensation planning cycle worksheet from BambooHR. |
| [Get Compensation Planning Worksheet CSV](actions/get-compensation-planning-worksheet-csv.md) | GET | Retrieves compensation planning worksheet csv from BambooHR. |
| [List Compensation Planning Cycle Admins](actions/list-compensation-planning-cycle-admins.md) | GET | Lists compensation planning cycle admins from BambooHR. |
| [List Compensation Planning Cycles](actions/list-compensation-planning-cycles.md) | GET | Lists compensation planning cycles from BambooHR. |
| [List Employees in Compensation Planning Cycle](actions/list-employees-in-compensation-planning-cycle.md) | GET | Lists employees in compensation planning cycle from BambooHR. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves custom field from BambooHR. |
| [List Archived Custom Fields](actions/list-archived-custom-fields.md) | GET | Lists archived custom fields from BambooHR. |
| [List Custom Field List Values](actions/list-custom-field-list-values.md) | GET | Lists custom field list values from BambooHR. |
| [List Custom Field Types](actions/list-custom-field-types.md) | GET | Lists custom field types from BambooHR. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Lists custom fields from BambooHR. |

### Custom Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Legacy Report Field Map](actions/get-legacy-report-field-map.md) | GET | Retrieves legacy report field map from BambooHR. |
| [Get Legacy Report ID Map](actions/get-legacy-report-id-map.md) | GET | Retrieves legacy report id map from BambooHR. |

### Custom Tables

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Table](actions/get-custom-table.md) | GET | Retrieves custom table from BambooHR. |
| [List Custom Tables](actions/list-custom-tables.md) | GET | Lists custom tables from BambooHR. |

### Dataset Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields from Dataset](actions/get-fields-from-dataset.md) | GET | Retrieves fields for a dataset from BambooHR. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Datasets](actions/get-datasets.md) | GET | Retrieves a list of datasets from BambooHR. |
| [Get Fields from Dataset V1 2](actions/get-fields-from-dataset-v12.md) | GET | Retrieves fields from dataset v1 2 from BambooHR. |
| [List Datasets V1 2](actions/list-datasets-v12.md) | GET | Lists datasets v1 2 from BambooHR. |

### Dependents

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Dependent](actions/get-employee-dependent.md) | GET | Retrieves one employee dependent from BambooHR. |
| [Get Employee Dependents](actions/get-employee-dependents.md) | GET | Retrieves employee dependent records from BambooHR. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST | Creates a new employee in BambooHR. |
| [Get Changed Employees](actions/get-changed-employees.md) | GET | Retrieves changed employee IDs from BambooHR. |
| [Get Employee](actions/get-employee.md) | GET | Retrieves details for one employee from BambooHR. |
| [List Employees](actions/list-employees.md) | GET | Retrieves a list of employees from BambooHR. |
| [Update Employee](actions/update-employee.md) | PUT | Updates an existing employee in BambooHR. |

### Employee Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee File](actions/get-employee-file.md) | GET | Retrieves employee file from BambooHR. |
| [List Employee Files](actions/list-employee-files.md) | GET | Lists employee files from BambooHR. |

### Employee Tables

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Table Rows](actions/list-employee-table-rows.md) | GET | Lists employee table rows from BambooHR. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Directory](actions/get-employee-directory.md) | GET | Retrieves the published employee directory from BambooHR. |

### Employeeverification

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Verification Integration Status](actions/get-employee-verification-integration-status.md) | GET | Retrieves employee verification integration status from BambooHR. |
| [List Employee Verification Records for an Employee](actions/list-employee-verification-records-for-an-employee.md) | GET | Lists employee verification records for an employee from BambooHR. |

### Employer Benefits

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Benefits](actions/get-company-benefits.md) | GET | Retrieves company benefit plans from BambooHR. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields](actions/get-fields.md) | GET | Retrieves available field metadata from BambooHR. |

### Goals

| Action | Method | Description |
| --- | --- | --- |
| [Get Alignable Goal Options](actions/get-alignable-goal-options.md) | GET | Retrieves alignable goal options from BambooHR. |
| [Get Goal Aggregate](actions/get-goal-aggregate.md) | GET | Retrieves goal aggregate from BambooHR. |
| [Get Goal Creation Permission](actions/get-goal-creation-permission.md) | GET | Retrieves goal creation permission from BambooHR. |
| [Get Goal Filters V1 2](actions/get-goal-filters-v12.md) | GET | Retrieves goal filters v1 2 from BambooHR. |
| [Get Goals Aggregate V1 2](actions/get-goals-aggregate-v12.md) | GET | Retrieves goals aggregate v1 2 from BambooHR. |
| [List Goal Comments](actions/list-goal-comments.md) | GET | Lists goal comments from BambooHR. |
| [List Goal Sharing Options](actions/list-goal-sharing-options.md) | GET | Lists goal sharing options from BambooHR. |
| [List Goals](actions/list-goals.md) | GET | Lists goals from BambooHR. |

### Holidays

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Holiday](actions/get-catalog-holiday.md) | GET | Retrieves catalog holiday from BambooHR. |
| [Get Company Holiday](actions/get-company-holiday.md) | GET | Retrieves company holiday from BambooHR. |
| [List Catalog Holidays](actions/list-catalog-holidays.md) | GET | Lists catalog holidays from BambooHR. |
| [List Company Holidays](actions/list-company-holidays.md) | GET | Lists company holidays from BambooHR. |

### Hours

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Tracking Record](actions/get-time-tracking-record.md) | GET | Retrieves time tracking record from BambooHR. |

### List Field

| Action | Method | Description |
| --- | --- | --- |
| [Get List Field Details](actions/get-list-field-details.md) | GET | Retrieves list field details from BambooHR. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Location](actions/get-job-location.md) | GET | Retrieves job location from BambooHR. |
| [List Job Locations](actions/list-job-locations.md) | GET | Lists job locations from BambooHR. |

### Onboarding

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Onboarding Experience by ID](actions/get-employee-onboarding-experience-by-id.md) | GET | Retrieves employee onboarding experience by id from BambooHR. |
| [Get New Hire Packet by ID](actions/get-new-hire-packet-by-id.md) | GET | Retrieves new hire packet by id from BambooHR. |
| [Get Welcome New Hires Widget](actions/get-welcome-new-hires-widget.md) | GET | Retrieves welcome new hires widget from BambooHR. |
| [List Employee Onboarding Experiences](actions/list-employee-onboarding-experiences.md) | GET | Lists employee onboarding experiences from BambooHR. |
| [List New Hire Packets](actions/list-new-hire-packets.md) | GET | Lists new hire packets from BambooHR. |

### Pay Grades & Bands

| Action | Method | Description |
| --- | --- | --- |
| [Get Compensation Level Group Status Counts](actions/get-compensation-level-group-status-counts.md) | GET | Retrieves compensation level group status counts from BambooHR. |
| [Get Job Titles and Level Assignments](actions/get-job-titles-and-level-assignments.md) | GET | Retrieves job titles and level assignments from BambooHR. |
| [Get Levels and Bands Review](actions/get-levels-and-bands-review.md) | GET | Retrieves levels and bands review from BambooHR. |
| [Get Levels and Bands Status](actions/get-levels-and-bands-status.md) | GET | Retrieves levels and bands status from BambooHR. |
| [Get Pay Bands](actions/get-pay-bands.md) | GET | Retrieves pay bands from BambooHR. |
| [Get Published Levels and Bands](actions/get-published-levels-and-bands.md) | GET | Retrieves published levels and bands from BambooHR. |
| [List Compensation Level Groups and Levels](actions/list-compensation-level-groups-and-levels.md) | GET | Lists compensation level groups and levels from BambooHR. |
| [List Job Titles with Employees](actions/list-job-titles-with-employees.md) | GET | Lists job titles with employees from BambooHR. |

### Photos

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Photo](actions/get-employee-photo.md) | GET | Retrieves employee photo from BambooHR. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Off Policies](actions/get-time-off-policies.md) | GET | Retrieves time off policies from BambooHR. |
| [Get Time Off Policies for Employee](actions/get-time-off-policies-for-employee.md) | GET | Retrieves time off policies for an employee from BambooHR. |

### Recognition Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Celebration Template Image Download URL](actions/get-celebration-template-image-download-url.md) | GET | Retrieves celebration template image download url from BambooHR. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Report by ID](actions/get-report-by-id.md) | GET | Retrieves a custom report from BambooHR by ID. |
| [Get Reports](actions/get-reports.md) | GET | Retrieves available custom reports from BambooHR. |

### Scheduling

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves schedule from BambooHR. |
| [Get Schedule PDF](actions/get-schedule-pdf.md) | GET | Retrieves schedule pdf from BambooHR. |
| [Get Shift](actions/get-shift.md) | GET | Retrieves shift from BambooHR. |
| [List Open Shifts](actions/list-open-shifts.md) | GET | Lists open shifts from BambooHR. |
| [List Schedules](actions/list-schedules.md) | GET | Lists schedules from BambooHR. |
| [List Scheduling Timezones](actions/list-scheduling-timezones.md) | GET | Lists scheduling timezones from BambooHR. |
| [List Shift Assessments](actions/list-shift-assessments.md) | GET | Lists shift assessments from BambooHR. |
| [List Shift Claims](actions/list-shift-claims.md) | GET | Lists shift claims from BambooHR. |
| [List Shifts](actions/list-shifts.md) | GET | Lists shifts from BambooHR. |

### Table Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Tabular Fields](actions/get-tabular-fields.md) | GET | Retrieves available tabular field metadata from BambooHR. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Off Category](actions/get-time-off-category.md) | GET | Retrieves time off category from BambooHR. |
| [Get Time Off Policy](actions/get-time-off-policy.md) | GET | Retrieves time off policy from BambooHR. |
| [Get Time Off Request](actions/get-time-off-request.md) | GET | Retrieves time off request from BambooHR. |
| [List Absent Employees](actions/list-absent-employees.md) | GET | Lists absent employees from BambooHR. |
| [List Employee Time Off Policies](actions/list-employee-time-off-policies.md) | GET | Lists employee time off policies from BambooHR. |
| [List Employee Time Off Policies V1 1](actions/list-employee-time-off-policies-v11.md) | GET | Lists employee time off policies v1 1 from BambooHR. |
| [List Time Off Policies](actions/list-time-off-policies.md) | GET | Lists time off policies from BambooHR. |
| [List Time Off Policy Versions](actions/list-time-off-policy-versions.md) | GET | Lists time off policy versions from BambooHR. |
| [List Time Off Request Comments](actions/list-time-off-request-comments.md) | GET | Lists time off request comments from BambooHR. |
| [List Time Off Requests](actions/list-time-off-requests.md) | GET | Lists time off requests from BambooHR. |

### Time Off Balances

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Off Balance](actions/get-time-off-balance.md) | GET | Retrieves an employee's time off balances from BambooHR. |

### Time Off Requests

| Action | Method | Description |
| --- | --- | --- |
| [Add Time Off Request](actions/add-time-off-request.md) | POST | Creates a time off request for an employee in BambooHR. |
| [Change Request Status](actions/change-request-status.md) | PUT | Updates a time off request status in BambooHR. |
| [Get Time Off Requests](actions/get-time-off-requests.md) | GET | Retrieves time off requests from BambooHR. |
| [Get Who's Out](actions/get-whos-out.md) | GET | Retrieves who's out entries and holidays from BambooHR. |

### Time Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Break](actions/get-break.md) | GET | Retrieves break from BambooHR. |
| [Get Break Policy](actions/get-break-policy.md) | GET | Retrieves break policy from BambooHR. |
| [Get Clock Entry](actions/get-clock-entry.md) | GET | Retrieves clock entry from BambooHR. |
| [Get Employee Enrollment](actions/get-employee-enrollment.md) | GET | Retrieves employee enrollment from BambooHR. |
| [Get Hour Entry](actions/get-hour-entry.md) | GET | Retrieves hour entry from BambooHR. |
| [Get Time Tracking Configuration](actions/get-time-tracking-configuration.md) | GET | Retrieves time tracking configuration from BambooHR. |
| [Get Time Tracking Import](actions/get-time-tracking-import.md) | GET | Retrieves time tracking import from BambooHR. |
| [Get Time Tracking Import Row](actions/get-time-tracking-import-row.md) | GET | Retrieves time tracking import row from BambooHR. |
| [Get Time Tracking Kiosk](actions/get-time-tracking-kiosk.md) | GET | Retrieves time tracking kiosk from BambooHR. |
| [Get Time Tracking Project](actions/get-time-tracking-project.md) | GET | Retrieves time tracking project from BambooHR. |
| [Get Time Tracking Shift Differential](actions/get-time-tracking-shift-differential.md) | GET | Retrieves time tracking shift differential from BambooHR. |
| [Get Time Tracking Task](actions/get-time-tracking-task.md) | GET | Retrieves time tracking task from BambooHR. |
| [Get Time Tracking Time Clock](actions/get-time-tracking-time-clock.md) | GET | Retrieves time tracking time clock from BambooHR. |
| [Get Timesheet](actions/get-timesheet.md) | GET | Retrieves timesheet from BambooHR. |
| [Get Timesheet Summary](actions/get-timesheet-summary.md) | GET | Retrieves timesheet summary from BambooHR. |
| [List Break Assessments](actions/list-break-assessments.md) | GET | Lists break assessments from BambooHR. |
| [List Break Policies](actions/list-break-policies.md) | GET | Lists break policies from BambooHR. |
| [List Break Policy Employees](actions/list-break-policy-employees.md) | GET | Lists break policy employees from BambooHR. |
| [List Breaks for Break Policy](actions/list-breaks-for-break-policy.md) | GET | Lists breaks for break policy from BambooHR. |
| [List Clock Entries](actions/list-clock-entries.md) | GET | Lists clock entries from BambooHR. |
| [List Employee Break Availabilities](actions/list-employee-break-availabilities.md) | GET | Lists employee break availabilities from BambooHR. |
| [List Employee Break Policies](actions/list-employee-break-policies.md) | GET | Lists employee break policies from BambooHR. |
| [List Enrolled Employees](actions/list-enrolled-employees.md) | GET | Lists enrolled employees from BambooHR. |
| [List Hour Entries](actions/list-hour-entries.md) | GET | Lists hour entries from BambooHR. |
| [List Time Tracking Configurations](actions/list-time-tracking-configurations.md) | GET | Lists time tracking configurations from BambooHR. |
| [List Time Tracking Import Rows](actions/list-time-tracking-import-rows.md) | GET | Lists time tracking import rows from BambooHR. |
| [List Time Tracking Imports](actions/list-time-tracking-imports.md) | GET | Lists time tracking imports from BambooHR. |
| [List Time Tracking Kiosks](actions/list-time-tracking-kiosks.md) | GET | Lists time tracking kiosks from BambooHR. |
| [List Time Tracking Project Tasks](actions/list-time-tracking-project-tasks.md) | GET | Lists time tracking project tasks from BambooHR. |
| [List Time Tracking Projects](actions/list-time-tracking-projects.md) | GET | Lists time tracking projects from BambooHR. |
| [List Time Tracking Shift Differentials](actions/list-time-tracking-shift-differentials.md) | GET | Lists time tracking shift differentials from BambooHR. |
| [List Time Tracking Time Clocks](actions/list-time-tracking-time-clocks.md) | GET | Lists time tracking time clocks from BambooHR. |
| [List Timesheet Entries](actions/list-timesheet-entries.md) | GET | Lists timesheet entries from BambooHR. |
| [List Timesheets](actions/list-timesheets.md) | GET | Lists timesheets from BambooHR. |

### Total Rewards

| Action | Method | Description |
| --- | --- | --- |
| [Get Printable Total Rewards Statement](actions/get-printable-total-rewards-statement.md) | GET | Retrieves printable total rewards statement from BambooHR. |
| [Get Total Rewards Profile Availability](actions/get-total-rewards-profile-availability.md) | GET | Retrieves total rewards profile availability from BambooHR. |
| [Get Total Rewards Statement](actions/get-total-rewards-statement.md) | GET | Retrieves total rewards statement from BambooHR. |

### Training

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Training Records](actions/list-employee-training-records.md) | GET | Lists employee training records from BambooHR. |
| [List Training Categories](actions/list-training-categories.md) | GET | Lists training categories from BambooHR. |
| [List Training Types](actions/list-training-types.md) | GET | Lists training types from BambooHR. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves a list of users from BambooHR. |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook from BambooHR. |
| [List Monitor Fields](actions/list-monitor-fields.md) | GET | Lists monitor fields from BambooHR. |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Lists webhook logs from BambooHR. |
| [List Webhook Post Fields](actions/list-webhook-post-fields.md) | GET | Lists webhook post fields from BambooHR. |
| [List Webhooks](actions/list-webhooks.md) | GET | Lists webhooks from BambooHR. |

