# Grand Avenue Software: Native API Reference

A consolidated summary of Grand Avenue Software's API configuration and 78 documented operations, with links to official documentation.

- **Official docs:** https://eval.grandavenue.com/MindCloud/Connector/ConfigureConnector.aspx?Params=ad3DaH4D696E64436C6F7564aHaLaH436F6E66696775726174696F6EaHaQ53797374656DaN
- **OpenAPI specification:** {{credentials.baseUrl}}/openapi.json
- **REST base URL:** `{baseUrl}`
- **XML base URL:** `{baseUrl}`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **OData Service Document URL:** `baseUrl` · required · Enter your OData Service Document URL.
Example:
`https://eval.grandavenue.com/MindCloud/odata/v2` 

To find yours, follow these steps:
1. Navigate to `Administrative Actions > Configure System > Configure Connector > Configure OData API`
2. Under `OData API Versions` right click and copy the `OData Service Document URL`.
3. Past the full URL here.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://grandavenue.atlassian.net/wiki/spaces/CS/pages/2033549314/How+do+I+Use+the+GAS+API)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use XML.

### XML

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use XML.

## Pagination

- **REST:** Use `$top` in the query string to set the page size (default 1000; accepted range 1–1000). Use `$skip` in the query string as the record offset.

## Sorting

- **REST:** Set the sort field with `$orderBy` in the query string. Use `ascending` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (78 documented)

| Operation | Method & path |
| --- | --- |
| [Get Activity Log Entry](actions/get-activity-log-entry.md) | `GET /ActivityLogEntries/:id` |
| [Get Assessment Result](actions/get-assessment-result.md) | `GET /AssessmentResults/:id` |
| [Get Associated Part](actions/get-associated-part.md) | `GET /AssociatedParts/:id` |
| [Get Associated Part related Process Item](actions/get-associated-part-process-item.md) | `GET /AssociatedParts/:id/ProcessItem` |
| [Get Audit Report](actions/get-audit-report.md) | `GET /AuditReports/:id` |
| [Get Capa Action](actions/get-capa-action.md) | `GET /CapaActions/:id` |
| [Get Capa Correction](actions/get-capa-correction.md) | `GET /CapaCorrections/:id` |
| [Get Capa Request](actions/get-capa-request.md) | `GET /CapaRequests/:id` |
| [Get Capa Root Cause](actions/get-capa-root-cause.md) | `GET /CapaRootCauses/:id` |
| [Get Change Request](actions/get-change-request.md) | `GET /ChangeRequests/:id` |
| [Get Complaint](actions/get-complaint.md) | `GET /Complaints/:id` |
| [Get Customer](actions/get-customer.md) | `GET /Customers/:id` |
| [Get Department](actions/get-department.md) | `GET /Departments/:id` |
| [Get Design Project](actions/get-design-project.md) | `GET /DesignProjects/:id` |
| [Get Deviation Request](actions/get-deviation-request.md) | `GET /DeviationRequests/:id` |
| [Get Document](actions/get-document.md) | `GET /Documents/:id` |
| [Get Equipment](actions/get-equipment.md) | `GET /Equipment/:id` |
| [Get Equipment Activity Entity Schedule](actions/get-equipment-activity-entity-schedule.md) | `GET /EquipmentEntityActivitySchedules/:id` |
| [Get Equipment Activity Record](actions/get-equipment-activity-record.md) | `GET /EquipmentActivityRecords/:id` |
| [Get Issue](actions/get-issue.md) | `GET /Issues/:id` |
| [Get Ncm Report](actions/get-ncm-report.md) | `GET /NcmReports/:id` |
| [Get Ncm Report Entry](actions/get-ncm-report-entry.md) | `GET /NcmReportEntries/:id` |
| [Get Part](actions/get-part.md) | `GET /Parts/:id` |
| [Get Process Impact](actions/get-process-impact.md) | `GET /ProcessImpacts/:id` |
| [Get Process Impact Process Item](actions/get-process-impact-process-item.md) | `GET /ProcessImpacts/:id/ProcessItem` |
| [Get Reporting Zone](actions/get-reporting-zone.md) | `GET /ReportingZones/:id` |
| [Get Requirement Collection](actions/get-requirement-collection.md) | `GET /RequirementCollections/:id` |
| [Get Requirement Design Input](actions/get-requirement-design-input.md) | `GET /RequirementDesignInputs/:id` |
| [Get Requirement Design Output](actions/get-requirement-design-output.md) | `GET /RequirementDesignOutputs/:id` |
| [Get Requirement User Need](actions/get-requirement-user-need.md) | `GET /RequirementUserNeeds/:id` |
| [Get Requirement Validation Result](actions/get-requirement-validation-result.md) | `GET /RequirementValidationResults/:id` |
| [Get Requirement Verification Result](actions/get-requirement-verification-result.md) | `GET /RequirementVerificationResults/:id` |
| [Get Risk Analysis](actions/get-risk-analysis.md) | `GET /RiskAnalyses/:id` |
| [Get Risk Analysis Failure Mode](actions/get-risk-analysis-failure-mode.md) | `GET /RiskAnalysisFailureModes/:id` |
| [Get Supplier](actions/get-supplier.md) | `GET /Suppliers/:id` |
| [Get Supplier Corrective Action Request](actions/get-supplier-corrective-action-request.md) | `GET /SupplierCorrectiveActionRequests/:id` |
| [Get Supplier Evaluation](actions/get-supplier-evaluation.md) | `GET /SupplierEvaluations/:id` |
| [Get Task Assignment](actions/get-task-assignment.md) | `GET /TaskAssignments/:id` |
| [Get Training Record](actions/get-training-record.md) | `GET /TrainingRecords/:id` |
| [Get User](actions/get-user.md) | `GET /Users/:id` |
| [List Activity Log Entries](actions/list-activity-log-entries.md) | `GET /ActivityLogEntries` |
| [List Assessment Results](actions/list-assessment-results.md) | `GET /AssessmentResults` |
| [List Associated Parts](actions/list-associated-parts.md) | `GET /AssociatedParts` |
| [List Audit Reports](actions/list-audit-reports.md) | `GET /AuditReports` |
| [List Capa Actions](actions/list-capa-actions.md) | `GET /CapaActions` |
| [List Capa Corrections](actions/list-capa-corrections.md) | `GET /CapaCorrections` |
| [List Capa Requests](actions/list-capa-requests.md) | `GET /CapaRequests` |
| [List Capa Root Causes](actions/list-capa-root-causes.md) | `GET /CapaRootCauses` |
| [List Change Requests](actions/list-change-requests.md) | `GET /ChangeRequests` |
| [List Complaints](actions/list-complaints.md) | `GET /Complaints` |
| [List Customers](actions/list-customers.md) | `GET /Customers` |
| [List Departments](actions/list-departments.md) | `GET /Departments` |
| [List Design Projects](actions/list-design-projects.md) | `GET /DesignProjects` |
| [List Deviation Requests](actions/list-deviation-requests.md) | `GET /DeviationRequests` |
| [List Documents](actions/list-documents.md) | `GET /Documents` |
| [List Equipment](actions/list-equipment.md) | `GET /Equipment` |
| [List Equipment Activity Entity Schedules](actions/list-equipment-activity-entity-schedules.md) | `GET /EquipmentEntityActivitySchedules` |
| [List Equipment Activity Records](actions/list-equipment-activity-records.md) | `GET /EquipmentActivityRecords` |
| [List Issues](actions/list-issues.md) | `GET /Issues` |
| [List Ncm Report Entries](actions/list-ncm-report-entries.md) | `GET /NcmReportEntries` |
| [List Ncm Reports](actions/list-ncm-reports.md) | `GET /NcmReports` |
| [List Parts](actions/list-parts.md) | `GET /Parts` |
| [List Process Impacts](actions/list-process-impacts.md) | `GET /ProcessImpacts` |
| [List Reporting Zones](actions/list-reporting-zones.md) | `GET /ReportingZones` |
| [List Requirement Collections](actions/list-requirement-collections.md) | `GET /RequirementCollections` |
| [List Requirement Design Inputs](actions/list-requirement-design-inputs.md) | `GET /RequirementDesignInputs` |
| [List Requirement Design Outputs](actions/list-requirement-design-outputs.md) | `GET /RequirementDesignOutputs` |
| [List Requirement User Needs](actions/list-requirement-user-needs.md) | `GET /RequirementUserNeeds` |
| [List Requirement Validation Results](actions/list-requirement-validation-results.md) | `GET /RequirementValidationResults` |
| [List Requirement Verification Results](actions/list-requirement-verification-results.md) | `GET /RequirementVerificationResults` |
| [List Risk Analyses](actions/list-risk-analyses.md) | `GET /RiskAnalyses` |
| [List Risk Analysis Failure Modes](actions/list-risk-analysis-failure-modes.md) | `GET /RiskAnalysisFailureModes` |
| [List Supplier Corrective Action Requests](actions/list-supplier-corrective-action-requests.md) | `GET /SupplierCorrectiveActionRequests` |
| [List Supplier Evaluations](actions/list-supplier-evaluations.md) | `GET /SupplierEvaluations` |
| [List Suppliers](actions/list-suppliers.md) | `GET /Suppliers` |
| [List Task Assignments](actions/list-task-assignments.md) | `GET /TaskAssignments` |
| [List Training Records](actions/list-training-records.md) | `GET /TrainingRecords` |
| [List Users](actions/list-users.md) | `GET /Users` |
