# Grand Avenue Software Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Grand Avenue Software expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-activity-log-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Grand Avenue Software actions that support pagination

- [List Activity Log Entries](actions/list-activity-log-entries.md)
- [List Assessment Results](actions/list-assessment-results.md)
- [List Associated Parts](actions/list-associated-parts.md)
- [List Audit Reports](actions/list-audit-reports.md)
- [List Capa Actions](actions/list-capa-actions.md)
- [List Capa Corrections](actions/list-capa-corrections.md)
- [List Capa Requests](actions/list-capa-requests.md)
- [List Capa Root Causes](actions/list-capa-root-causes.md)
- [List Change Requests](actions/list-change-requests.md)
- [List Complaints](actions/list-complaints.md)
- [List Customers](actions/list-customers.md)
- [List Departments](actions/list-departments.md)
- [List Design Projects](actions/list-design-projects.md)
- [List Deviation Requests](actions/list-deviation-requests.md)
- [List Documents](actions/list-documents.md)
- [List Equipment](actions/list-equipment.md)
- [List Equipment Activity Entity Schedules](actions/list-equipment-activity-entity-schedules.md)
- [List Equipment Activity Records](actions/list-equipment-activity-records.md)
- [List Issues](actions/list-issues.md)
- [List Ncm Report Entries](actions/list-ncm-report-entries.md)
- [List Ncm Reports](actions/list-ncm-reports.md)
- [List Parts](actions/list-parts.md)
- [List Process Impacts](actions/list-process-impacts.md)
- [List Reporting Zones](actions/list-reporting-zones.md)
- [List Requirement Collections](actions/list-requirement-collections.md)
- [List Requirement Design Inputs](actions/list-requirement-design-inputs.md)
- [List Requirement Design Outputs](actions/list-requirement-design-outputs.md)
- [List Requirement User Needs](actions/list-requirement-user-needs.md)
- [List Requirement Validation Results](actions/list-requirement-validation-results.md)
- [List Requirement Verification Results](actions/list-requirement-verification-results.md)
- [List Risk Analyses](actions/list-risk-analyses.md)
- [List Risk Analysis Failure Modes](actions/list-risk-analysis-failure-modes.md)
- [List Supplier Corrective Action Requests](actions/list-supplier-corrective-action-requests.md)
- [List Supplier Evaluations](actions/list-supplier-evaluations.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Task Assignments](actions/list-task-assignments.md)
- [List Training Records](actions/list-training-records.md)
- [List Users](actions/list-users.md)
