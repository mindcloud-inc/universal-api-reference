# <img src="https://images.mindcloud.co/apps/icons/id-t0un3aej-logos_1774898499173.jpeg" alt="MyHR logo" width="28" height="28"> MyHR: Universal API

myHR is an HR management platform for employee data, leave, absences, expenses, training, scheduling, and related HR workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myHR/latest
- **Category:** Human Resources / HRIS
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.myhr.lu/
- **Vendor API docs:** https://www.myhr-api.lu/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employment Statuses](actions/list-employment-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employment-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Assets For Employee](actions/list-employee-assets-for-employee.md) | GET |  |

### Bonus

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Bonuses For Employee](actions/list-employee-bonuses-for-employee.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Company Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Company Assets](actions/list-company-assets.md) | GET |  |

### Company Public Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Company Public Holidays](actions/list-company-public-holidays.md) | GET |  |

### Company Time Off Reason

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Time Off Reason](actions/create-company-time-off-reason.md) | POST |  |
| [List Company Time Off Reasons](actions/list-company-time-off-reasons.md) | GET |  |
| [Update Company Time Off Reason](actions/update-company-time-off-reason.md) | PUT |  |

### Compensation

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Compensations For Employee](actions/list-employee-compensations-for-employee.md) | GET |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST |  |
| [Get Employee By Foreign Key](actions/get-employee-by-foreign-key.md) | GET |  |
| [Get Employee By PID](actions/get-employee-by-pid.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [Update Employee](actions/update-employee.md) | PUT |  |

### Employee Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee Address](actions/create-employee-address.md) | POST |  |
| [Get Current Employee Address](actions/get-current-employee-address.md) | GET |  |
| [List Employee Addresses](actions/list-employee-addresses.md) | GET |  |
| [Update Employee Address](actions/update-employee-address.md) | PUT |  |

### Employee Skill

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Skills For Employee](actions/list-employee-skills-for-employee.md) | GET |  |

### Employee Status

| Action | Method | Description |
| --- | --- | --- |
| [Activate Employee](actions/activate-employee.md) | PUT |  |
| [Deactivate Employee](actions/deactivate-employee.md) | PUT |  |
| [Get Current Employee Status](actions/get-current-employee-status.md) | GET |  |
| [List Employee Statuses](actions/list-employee-statuses.md) | GET |  |
| [Terminate Employee](actions/terminate-employee.md) | PUT |  |

### Employment Status

| Action | Method | Description |
| --- | --- | --- |
| [List Employment Statuses](actions/list-employment-statuses.md) | GET |  |

### Expense Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Expense Note](actions/get-employee-expense-note.md) | GET |  |
| [List Employee Expense Notes](actions/list-employee-expense-notes.md) | GET |  |

### Expense Note Expense

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Note Expenses For Expense Note](actions/list-expense-note-expenses-for-expense-note.md) | GET |  |

### Punch Clock Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Punch Clock Balance](actions/get-punch-clock-balance.md) | GET |  |

### Punch Clock Clockin

| Action | Method | Description |
| --- | --- | --- |
| [List Punch Clock Clockins](actions/list-punch-clock-clockins.md) | GET |  |

### Time Off Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee Time Off Request](actions/create-employee-time-off-request.md) | POST |  |
| [Get Employee Time Off Request](actions/get-employee-time-off-request.md) | GET |  |
| [List Employee Time Off Requests](actions/list-employee-time-off-requests.md) | GET |  |
| [List Employee Time Off Requests For Employee](actions/list-employee-time-off-requests-for-employee.md) | GET |  |
| [Move Employee Time Off Request To Trashbox](actions/move-employee-time-off-request-to-trashbox.md) | DELETE |  |
| [Update Employee Time Off Request Status](actions/update-employee-time-off-request-status.md) | PUT |  |

### Time Off Request Day

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Time Off Request Days](actions/list-employee-time-off-request-days.md) | GET |  |
| [List Time Off Request Days For Employee](actions/list-time-off-request-days-for-employee.md) | GET |  |
| [List Time Off Request Days For Request](actions/list-time-off-request-days-for-request.md) | GET |  |

### Time Off Request Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Time Off Request Status](actions/get-employee-time-off-request-status.md) | GET |  |

### Training Course

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Training Courses For Employee](actions/list-employee-training-courses-for-employee.md) | GET |  |

