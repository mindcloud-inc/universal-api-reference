# <img src="https://images.mindcloud.co/apps/icons/hr-icon_1774644372277.jpeg" alt="TalentHR logo" width="28" height="28"> TalentHR: Universal API

Manage employee records, directory, ATS applicants, time off, benefits, documents, tasks, and assets in TalentHR.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/talentHR/latest
- **Category:** Human Resources / HRIS
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.talenthr.io/
- **Vendor API docs:** https://apidocs.talenthr.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Directory](actions/get-directory.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Applicant

| Action | Method | Description |
| --- | --- | --- |
| [Get Applicant](actions/get-applicant.md) | GET | Retrieves an applicant from TalentHR. |

### Benefit

| Action | Method | Description |
| --- | --- | --- |
| [List Benefits](actions/list-benefits.md) | GET | Retrieves benefits from TalentHR. |

### Benefit Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Benefit Category](actions/create-benefit-category.md) | POST | Creates a new benefit category in TalentHR. |
| [List Benefit Categories](actions/list-benefit-categories.md) | GET | Retrieves benefit categories from TalentHR. |
| [Update Benefit Category](actions/update-benefit-category.md) | PUT | Updates an existing benefit category in TalentHR. |

### Benefit Filters

| Action | Method | Description |
| --- | --- | --- |
| [Get Benefit Filters](actions/get-benefit-filters.md) | GET | Retrieves benefit filters from TalentHR. |

### Blocked Time Off

| Action | Method | Description |
| --- | --- | --- |
| [List Time Off Blocked Periods](actions/list-time-off-blocked-periods.md) | GET | Retrieves blocked time off periods from TalentHR. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves candidates from TalentHR. |

### Company Document

| Action | Method | Description |
| --- | --- | --- |
| [List Company Documents](actions/list-company-documents.md) | GET | Retrieves company documents from TalentHR. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported countries from TalentHR. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from TalentHR. |

### Directory Filter

| Action | Method | Description |
| --- | --- | --- |
| [Get Directory Filters](actions/get-directory-filters.md) | GET | Retrieves employee directory filters from TalentHR. |

### Division

| Action | Method | Description |
| --- | --- | --- |
| [Create Division](actions/create-division.md) | POST | Creates a new division in TalentHR. |
| [List Divisions](actions/list-divisions.md) | GET | Retrieves divisions from TalentHR. |
| [Update Division](actions/update-division.md) | PUT | Updates an existing division in TalentHR. |

### Education Level

| Action | Method | Description |
| --- | --- | --- |
| [List Education Levels](actions/list-education-levels.md) | GET | Retrieves education levels from TalentHR. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Directory](actions/get-directory.md) | GET | Retrieves the employee directory from TalentHR. |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from TalentHR. |
| [Get Employee Job Info](actions/get-employee-job-info.md) | GET | Retrieves employee job details from TalentHR. |
| [List Employee Managers](actions/list-employee-managers.md) | GET | Retrieves an employee's managers from TalentHR. |

### Employee Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Assets](actions/list-employee-assets.md) | GET | Retrieves an employee's assets from TalentHR. |

### Employee Available Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Available Assets](actions/list-employee-available-assets.md) | GET | Retrieves an employee's available assets from TalentHR. |

### Employee Benefit

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Benefits](actions/list-employee-benefits.md) | GET | Retrieves an employee's benefits from TalentHR. |

### Employee Completed Task

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Completed Tasks](actions/list-employee-completed-tasks.md) | GET | Retrieves an employee's completed tasks from TalentHR. |

### Employee Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Custom Fields](actions/list-employee-custom-fields.md) | GET | Retrieves an employee's custom fields from TalentHR. |

### Employee Document

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Documents](actions/list-employee-documents.md) | GET | Retrieves an employee's documents from TalentHR. |

### Employee Pending Task

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Pending Tasks](actions/list-employee-pending-tasks.md) | GET | Retrieves an employee's pending tasks from TalentHR. |

### Employee Time Off Budget

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Time Off Budgets](actions/list-employee-time-off-budgets.md) | GET | Retrieves an employee's time off budgets from TalentHR. |

### Employee Time Off Request

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Time Off Requests](actions/list-employee-time-off-requests.md) | GET | Retrieves an employee's time off requests from TalentHR. |

### Employment Status

| Action | Method | Description |
| --- | --- | --- |
| [List Employment Statuses](actions/list-employment-statuses.md) | GET | Retrieves employment statuses from TalentHR. |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Create Holiday](actions/create-holiday.md) | POST | Creates a new holiday in TalentHR. |
| [List Holidays](actions/list-holidays.md) | GET | Retrieves holidays from TalentHR. |
| [Update Holiday](actions/update-holiday.md) | PUT | Updates an existing holiday in TalentHR. |

### Holiday Year

| Action | Method | Description |
| --- | --- | --- |
| [List Holiday Years](actions/list-holiday-years.md) | GET | Retrieves holiday years from TalentHR. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Title](actions/create-job-title.md) | POST | Creates a new job title in TalentHR. |
| [Update Job Title](actions/update-job-title.md) | PUT | Updates an existing job title in TalentHR. |

### Job Position

| Action | Method | Description |
| --- | --- | --- |
| [List Job Positions](actions/list-job-positions.md) | GET | Retrieves job positions from TalentHR. |

### Job Position Applicant

| Action | Method | Description |
| --- | --- | --- |
| [List Job Position Applicants](actions/list-job-position-applicants.md) | GET | Retrieves applicants for a TalentHR job position. |

### Job Title

| Action | Method | Description |
| --- | --- | --- |
| [List Job Titles](actions/list-job-titles.md) | GET | Retrieves job titles from TalentHR. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves supported languages from TalentHR. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from TalentHR. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in TalentHR. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in TalentHR. |

### Nationality

| Action | Method | Description |
| --- | --- | --- |
| [List Nationalities](actions/list-nationalities.md) | GET | Retrieves supported nationalities from TalentHR. |

### Organization Chart Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Chart](actions/get-organization-chart.md) | GET | Retrieves the organization chart from TalentHR. |

### Published Job Position

| Action | Method | Description |
| --- | --- | --- |
| [List Published Job Positions](actions/list-published-job-positions.md) | GET | Retrieves published job positions from TalentHR. |

### Relationship Type

| Action | Method | Description |
| --- | --- | --- |
| [List Relationship Types](actions/list-relationship-types.md) | GET | Retrieves relationship types from TalentHR. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Off Blocked Period](actions/create-time-off-blocked-period.md) | POST | Creates a new blocked time off period in TalentHR. |
| [Create Time Off Type](actions/create-time-off-type.md) | POST | Creates a new time off type in TalentHR. |
| [Update Time Off Blocked Period](actions/update-time-off-blocked-period.md) | PUT | Updates an existing blocked time off period in TalentHR. |

### Time Off Type

| Action | Method | Description |
| --- | --- | --- |
| [List Time Off Types](actions/list-time-off-types.md) | GET | Retrieves time off types from TalentHR. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Timezones](actions/list-timezones.md) | GET | Retrieves supported timezones from TalentHR. |

