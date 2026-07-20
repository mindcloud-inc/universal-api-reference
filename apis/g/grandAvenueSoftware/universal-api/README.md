# <img src="https://images.mindcloud.co/apps/icons/gas-mc-app-icon-1_1781300135664.png" alt="Grand Avenue Software logo" width="28" height="28"> Grand Avenue Software: Universal API

Purpose-built eQMS for medical device and life science teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grandAvenueSoftware/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 78
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://grandavenue.com/
- **Vendor API docs:** https://eval.grandavenue.com/MindCloud/Connector/ConfigureConnector.aspx?Params=ad3DaH4D696E64436C6F7564aHaLaH436F6E66696775726174696F6EaHaQ53797374656DaN

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Activity Log Entry](actions/get-activity-log-entry.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (78)

### Activity Log Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Log Entry](actions/get-activity-log-entry.md) | GET | Retrieves an activity log entry from Grand Avenue Software by ID. |
| [List Activity Log Entries](actions/list-activity-log-entries.md) | GET | Retrieves activity log entries from Grand Avenue Software. |

### Assessment Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Assessment Result](actions/get-assessment-result.md) | GET | Retrieves an assessment result from Grand Avenue Software by ID. |
| [List Assessment Results](actions/list-assessment-results.md) | GET | Retrieves assessment results from Grand Avenue Software. |

### Associated Parts

| Action | Method | Description |
| --- | --- | --- |
| [Get Associated Part](actions/get-associated-part.md) | GET | Retrieves an associated part from Grand Avenue Software by ID. |
| [Get Associated Part related Process Item](actions/get-associated-part-process-item.md) | GET | Retrieves an associated part's related process item from Grand Avenue Software. |
| [List Associated Parts](actions/list-associated-parts.md) | GET | Retrieves associated parts from Grand Avenue Software. |

### Audit Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Report](actions/get-audit-report.md) | GET | Retrieves an audit report from Grand Avenue Software by ID. |
| [List Audit Reports](actions/list-audit-reports.md) | GET | Retrieves audit reports from Grand Avenue Software. |

### Capa

| Action | Method | Description |
| --- | --- | --- |
| [Get Capa Action](actions/get-capa-action.md) | GET | Retrieves a CAPA action from Grand Avenue Software by ID. |
| [Get Capa Correction](actions/get-capa-correction.md) | GET | Retrieves a CAPA correction from Grand Avenue Software by ID. |
| [Get Capa Request](actions/get-capa-request.md) | GET | Retrieves a CAPA request from Grand Avenue Software by ID. |
| [Get Capa Root Cause](actions/get-capa-root-cause.md) | GET | Retrieves a CAPA root cause from Grand Avenue Software by ID. |
| [List Capa Actions](actions/list-capa-actions.md) | GET | Retrieves CAPA actions from Grand Avenue Software. |
| [List Capa Corrections](actions/list-capa-corrections.md) | GET | Retrieves CAPA corrections from Grand Avenue Software. |
| [List Capa Requests](actions/list-capa-requests.md) | GET | Retrieves CAPA requests from Grand Avenue Software. |
| [List Capa Root Causes](actions/list-capa-root-causes.md) | GET | Retrieves CAPA root causes from Grand Avenue Software. |

### Change Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Change Request](actions/get-change-request.md) | GET | Retrieves a change request from Grand Avenue Software by ID. |
| [List Change Requests](actions/list-change-requests.md) | GET | Retrieves change requests from Grand Avenue Software. |

### Complaints

| Action | Method | Description |
| --- | --- | --- |
| [Get Complaint](actions/get-complaint.md) | GET | Retrieves a complaint from Grand Avenue Software by ID. |
| [List Complaints](actions/list-complaints.md) | GET | Retrieves complaints from Grand Avenue Software. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Grand Avenue Software by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Grand Avenue Software. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Get Department](actions/get-department.md) | GET | Retrieves a department from Grand Avenue Software by ID. |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from Grand Avenue Software. |

### Design Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Design Project](actions/get-design-project.md) | GET | Retrieves a design project from Grand Avenue Software by ID. |
| [List Design Projects](actions/list-design-projects.md) | GET | Retrieves design projects from Grand Avenue Software. |

### Deviation Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Deviation Request](actions/get-deviation-request.md) | GET | Retrieves a deviation request from Grand Avenue Software by ID. |
| [List Deviation Requests](actions/list-deviation-requests.md) | GET | Retrieves deviation requests from Grand Avenue Software. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Grand Avenue Software by ID. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Grand Avenue Software. |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment](actions/get-equipment.md) | GET | Retrieves equipment from Grand Avenue Software by ID. |
| [Get Equipment Activity Entity Schedule](actions/get-equipment-activity-entity-schedule.md) | GET | Retrieves an equipment activity entity schedule from Grand Avenue Software by ID. |
| [Get Equipment Activity Record](actions/get-equipment-activity-record.md) | GET | Retrieves an equipment activity record from Grand Avenue Software by ID. |
| [List Equipment](actions/list-equipment.md) | GET | Retrieves equipment from Grand Avenue Software. |
| [List Equipment Activity Entity Schedules](actions/list-equipment-activity-entity-schedules.md) | GET | Retrieves equipment activity entity schedules from Grand Avenue Software. |
| [List Equipment Activity Records](actions/list-equipment-activity-records.md) | GET | Retrieves equipment activity records from Grand Avenue Software. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Grand Avenue Software by ID. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues from Grand Avenue Software. |

### Ncm Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Ncm Report](actions/get-ncm-report.md) | GET | Retrieves an NCM report from Grand Avenue Software by ID. |
| [Get Ncm Report Entry](actions/get-ncm-report-entry.md) | GET | Retrieves an NCM report entry from Grand Avenue Software by ID. |
| [List Ncm Report Entries](actions/list-ncm-report-entries.md) | GET | Retrieves NCM report entries from Grand Avenue Software. |
| [List Ncm Reports](actions/list-ncm-reports.md) | GET | Retrieves NCM reports from Grand Avenue Software. |

### Parts

| Action | Method | Description |
| --- | --- | --- |
| [Get Part](actions/get-part.md) | GET | Retrieves a part from Grand Avenue Software by ID. |
| [List Parts](actions/list-parts.md) | GET | Retrieves parts from Grand Avenue Software. |

### Process Impacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Process Impact](actions/get-process-impact.md) | GET | Retrieves a process impact from Grand Avenue Software by ID. |
| [Get Process Impact Process Item](actions/get-process-impact-process-item.md) | GET | Retrieves a process impact's related process item from Grand Avenue Software. |
| [List Process Impacts](actions/list-process-impacts.md) | GET | Retrieves process impacts from Grand Avenue Software. |

### Reporting Zones

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting Zone](actions/get-reporting-zone.md) | GET | Retrieves a reporting zone from Grand Avenue Software by ID. |
| [List Reporting Zones](actions/list-reporting-zones.md) | GET | Retrieves reporting zones from Grand Avenue Software. |

### Requirements

| Action | Method | Description |
| --- | --- | --- |
| [Get Requirement Collection](actions/get-requirement-collection.md) | GET | Retrieves a requirement collection from Grand Avenue Software by ID. |
| [Get Requirement Design Input](actions/get-requirement-design-input.md) | GET | Retrieves a requirement design input from Grand Avenue Software by ID. |
| [Get Requirement Design Output](actions/get-requirement-design-output.md) | GET | Retrieves a requirement design output from Grand Avenue Software by ID. |
| [Get Requirement User Need](actions/get-requirement-user-need.md) | GET | Retrieves a requirement user need from Grand Avenue Software by ID. |
| [Get Requirement Validation Result](actions/get-requirement-validation-result.md) | GET | Retrieves a requirement validation result from Grand Avenue Software by ID. |
| [Get Requirement Verification Result](actions/get-requirement-verification-result.md) | GET | Retrieves a requirement verification result from Grand Avenue Software by ID. |
| [List Requirement Collections](actions/list-requirement-collections.md) | GET | Retrieves requirement collections from Grand Avenue Software. |
| [List Requirement Design Inputs](actions/list-requirement-design-inputs.md) | GET | Retrieves requirement design inputs from Grand Avenue Software. |
| [List Requirement Design Outputs](actions/list-requirement-design-outputs.md) | GET | Retrieves requirement design outputs from Grand Avenue Software. |
| [List Requirement User Needs](actions/list-requirement-user-needs.md) | GET | Retrieves requirement user needs from Grand Avenue Software. |
| [List Requirement Validation Results](actions/list-requirement-validation-results.md) | GET | Retrieves requirement validation results from Grand Avenue Software. |
| [List Requirement Verification Results](actions/list-requirement-verification-results.md) | GET | Retrieves requirement verification results from Grand Avenue Software. |

### Risk Analyses

| Action | Method | Description |
| --- | --- | --- |
| [Get Risk Analysis](actions/get-risk-analysis.md) | GET | Retrieves a risk analysis from Grand Avenue Software by ID. |
| [Get Risk Analysis Failure Mode](actions/get-risk-analysis-failure-mode.md) | GET | Retrieves a risk analysis failure mode from Grand Avenue Software by ID. |
| [List Risk Analyses](actions/list-risk-analyses.md) | GET | Retrieves risk analyses from Grand Avenue Software. |
| [List Risk Analysis Failure Modes](actions/list-risk-analysis-failure-modes.md) | GET | Retrieves risk analysis failure modes from Grand Avenue Software. |

### Suppliers

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Grand Avenue Software by ID. |
| [Get Supplier Corrective Action Request](actions/get-supplier-corrective-action-request.md) | GET | Retrieves a supplier corrective action request from Grand Avenue Software by ID. |
| [Get Supplier Evaluation](actions/get-supplier-evaluation.md) | GET | Retrieves a supplier evaluation from Grand Avenue Software by ID. |
| [List Supplier Corrective Action Requests](actions/list-supplier-corrective-action-requests.md) | GET | Retrieves supplier corrective action requests from Grand Avenue Software. |
| [List Supplier Evaluations](actions/list-supplier-evaluations.md) | GET | Retrieves supplier evaluations from Grand Avenue Software. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Grand Avenue Software. |

### Task Assignments

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Assignment](actions/get-task-assignment.md) | GET | Retrieves a task assignment from Grand Avenue Software by ID. |
| [List Task Assignments](actions/list-task-assignments.md) | GET | Retrieves task assignments from Grand Avenue Software. |

### Training Records

| Action | Method | Description |
| --- | --- | --- |
| [Get Training Record](actions/get-training-record.md) | GET | Retrieves a training record from Grand Avenue Software by ID. |
| [List Training Records](actions/list-training-records.md) | GET | Retrieves training records from Grand Avenue Software. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Grand Avenue Software by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Grand Avenue Software. |

