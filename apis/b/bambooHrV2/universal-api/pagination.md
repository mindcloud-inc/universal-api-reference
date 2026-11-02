# BambooHR Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model BambooHR expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-fields-from-dataset-v12?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## BambooHR actions that support pagination

- [Get Fields from Dataset V1 2](actions/get-fields-from-dataset-v12.md)
- [Get Member Benefits](actions/get-member-benefits.md)
- [List Absent Employees](actions/list-absent-employees.md)
- [List Archived Custom Fields](actions/list-archived-custom-fields.md)
- [List Break Assessments](actions/list-break-assessments.md)
- [List Break Policies](actions/list-break-policies.md)
- [List Break Policy Employees](actions/list-break-policy-employees.md)
- [List Breaks for Break Policy](actions/list-breaks-for-break-policy.md)
- [List Calendar Events](actions/list-calendar-events.md)
- [List Catalog Holidays](actions/list-catalog-holidays.md)
- [List Clock Entries](actions/list-clock-entries.md)
- [List Company Holidays](actions/list-company-holidays.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Custom Tables](actions/list-custom-tables.md)
- [List Employee Break Policies](actions/list-employee-break-policies.md)
- [List Employee Time Off Policies](actions/list-employee-time-off-policies.md)
- [List Employees](actions/list-employees.md)
- [List Enrolled Employees](actions/list-enrolled-employees.md)
- [List Hour Entries](actions/list-hour-entries.md)
- [List Job Locations](actions/list-job-locations.md)
- [List New Hire Packets](actions/list-new-hire-packets.md)
- [List Open Shifts](actions/list-open-shifts.md)
- [List Schedules](actions/list-schedules.md)
- [List Scheduling Timezones](actions/list-scheduling-timezones.md)
- [List Shift Assessments](actions/list-shift-assessments.md)
- [List Shift Claims](actions/list-shift-claims.md)
- [List Shifts](actions/list-shifts.md)
- [List Time Off Policies](actions/list-time-off-policies.md)
- [List Time Off Policy Versions](actions/list-time-off-policy-versions.md)
- [List Time Off Requests](actions/list-time-off-requests.md)
- [List Time Tracking Configurations](actions/list-time-tracking-configurations.md)
- [List Time Tracking Import Rows](actions/list-time-tracking-import-rows.md)
- [List Time Tracking Imports](actions/list-time-tracking-imports.md)
- [List Time Tracking Kiosks](actions/list-time-tracking-kiosks.md)
- [List Time Tracking Project Tasks](actions/list-time-tracking-project-tasks.md)
- [List Time Tracking Projects](actions/list-time-tracking-projects.md)
- [List Time Tracking Shift Differentials](actions/list-time-tracking-shift-differentials.md)
- [List Time Tracking Time Clocks](actions/list-time-tracking-time-clocks.md)
- [List Timesheets](actions/list-timesheets.md)
- [List Timezones](actions/list-timezones.md)
