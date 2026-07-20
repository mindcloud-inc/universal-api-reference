# <img src="https://images.mindcloud.co/apps/icons/bamboo-hr_1773069235672.png" alt="BambooHR logo" width="28" height="28"> BambooHR: Universal API

Manage employee records, time off, benefits, and directory data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bambooHrV2/latest
- **Category:** Human Resources / HRIS
- **Actions:** 31
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

## Actions (31)

### Benefits

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Benefits](actions/get-employee-benefits.md) | GET | Retrieves employee benefit enrollments from BambooHR. |
| [Get Member Benefit Events](actions/get-member-benefit-events.md) | GET | Retrieves member benefit events from BambooHR. |
| [Get Member Benefits](actions/get-member-benefits.md) | GET | Retrieves member benefit enrollments from BambooHR. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Benefit Coverages](actions/get-benefit-coverages.md) | GET | Retrieves benefit coverage options from BambooHR. |
| [Get Benefit Deduction Types](actions/get-benefit-deduction-types.md) | GET | Retrieves benefit deduction types from BambooHR. |
| [Get Time Off Types](actions/get-time-off-types.md) | GET | Retrieves time off types from BambooHR. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Information](actions/get-company-information.md) | GET | Retrieves company profile information from BambooHR. |

### Dataset Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields from Dataset](actions/get-fields-from-dataset.md) | GET | Retrieves fields for a dataset from BambooHR. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Datasets](actions/get-datasets.md) | GET | Retrieves a list of datasets from BambooHR. |

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

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Directory](actions/get-employee-directory.md) | GET | Retrieves the published employee directory from BambooHR. |

### Employer Benefits

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Benefits](actions/get-company-benefits.md) | GET | Retrieves company benefit plans from BambooHR. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields](actions/get-fields.md) | GET | Retrieves available field metadata from BambooHR. |

### List Field

| Action | Method | Description |
| --- | --- | --- |
| [Get List Field Details](actions/get-list-field-details.md) | GET | Retrieves list field details from BambooHR. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Off Policies](actions/get-time-off-policies.md) | GET | Retrieves time off policies from BambooHR. |
| [Get Time Off Policies for Employee](actions/get-time-off-policies-for-employee.md) | GET | Retrieves time off policies for an employee from BambooHR. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Report by ID](actions/get-report-by-id.md) | GET | Retrieves a custom report from BambooHR by ID. |
| [Get Reports](actions/get-reports.md) | GET | Retrieves available custom reports from BambooHR. |

### Table Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Tabular Fields](actions/get-tabular-fields.md) | GET | Retrieves available tabular field metadata from BambooHR. |

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

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves a list of users from BambooHR. |

