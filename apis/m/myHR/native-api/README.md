# MyHR: Native API Reference

A consolidated summary of MyHR's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://www.myhr-api.lu/
- **API base URL:** `https://mindcloud.myhr.lu/api/v2`

## Authentication

### Basic Auth

Connect with the API username and API password generated in Company > Software Settings > Security > API Access.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.myhr-api.lu/)

## API conventions

Responses from this API use JSON. The total page count is read from `pagination.numPages`. The current page number is read from `pagination.currentPage`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Employee](actions/activate-employee.md) | `POST /hr/employees/:employee_pid/statuses/do/activate` | [docs](https://www.postman.com/myhr-api/request/27799381-7598cfad-13d2-4a61-a46e-18f845daf442) |
| [Create Company Time Off Reason](actions/create-company-time-off-reason.md) | `POST /company_timeoff_reasons` | [docs](https://www.postman.com/myhr-api/request/27799381-85a68433-7046-4b4f-bb3d-2b3e05dd53d5) |
| [Create Employee](actions/create-employee.md) | `POST /employees` | [docs](https://www.postman.com/myhr-api/request/27799381-8fa91af3-bd8e-44aa-bfe8-c48a483ba055) |
| [Create Employee Address](actions/create-employee-address.md) | `POST /hr/employees/:employee_pid/addresses` | [docs](https://www.postman.com/myhr-api/request/27799381-fae7a3d8-b769-43b9-b00b-91a098eaf06a) |
| [Create Employee Time Off Request](actions/create-employee-time-off-request.md) | `POST /employees/:employee_pid/employee_timeoff_request` | [docs](https://www.postman.com/myhr-api/request/27799381-f56798cd-2a03-4638-9ff6-5b05b4034bca) |
| [Deactivate Employee](actions/deactivate-employee.md) | `POST /hr/employees/:employee_pid/statuses/do/deactivate` | [docs](https://www.postman.com/myhr-api/request/27799381-e8ffa5f2-1172-4773-a96c-742e9edb6ba7) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://www.postman.com/myhr-api/request/27799381-57e3399c-f2e2-4a42-a8a5-7c90ffdd71b3) |
| [Get Current Employee Address](actions/get-current-employee-address.md) | `GET /hr/employees/:employee_pid/addresses/current` | [docs](https://www.postman.com/myhr-api/request/27799381-c1e8ad06-ec90-4559-b759-4e15cf38b175) |
| [Get Current Employee Status](actions/get-current-employee-status.md) | `GET /hr/employees/:employee_pid/statuses/current` | [docs](https://www.postman.com/myhr-api/request/27799381-99ffa193-4955-4793-9783-04605012ad03) |
| [Get Employee By Foreign Key](actions/get-employee-by-foreign-key.md) | `GET /employees/@` | [docs](https://www.postman.com/myhr-api/request/27799381-792e87f4-f1f6-4cf6-91d5-d1ef5e9c9564) |
| [Get Employee By PID](actions/get-employee-by-pid.md) | `GET /employees/:employee_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-87c948ef-ce21-4a95-995e-ab4f46b5b0c8) |
| [Get Employee Expense Note](actions/get-employee-expense-note.md) | `GET /employee_expense_notes/:employee_expense_note_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-0bc4b337-a36b-4afd-8171-9dec1adf4f20) |
| [Get Employee Time Off Request](actions/get-employee-time-off-request.md) | `GET /employee_timeoff_requests/:employee_timeoff_request_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-c4df1adb-bfc7-4a51-bca2-71cc9654ff08) |
| [Get Employee Time Off Request Status](actions/get-employee-time-off-request-status.md) | `GET /employee_timeoff_requests/:employee_timeoff_request_pid/status` | [docs](https://www.postman.com/myhr-api/request/27799381-372cb166-0647-4d9d-8784-8abcea642269) |
| [Get Punch Clock Balance](actions/get-punch-clock-balance.md) | `GET /employees/:employee_pid/punch-clock/balance` | [docs](https://www.postman.com/myhr-api/request/27799381-9ccf0f16-508f-45bc-9af2-54fcec9fa3a8) |
| [List Company Assets](actions/list-company-assets.md) | `GET /company_assets` | [docs](https://www.postman.com/myhr-api/request/27799381-bf098017-da21-4d10-90db-93beb5357812) |
| [List Company Public Holidays](actions/list-company-public-holidays.md) | `GET /company_public_holidays` | [docs](https://www.postman.com/myhr-api/request/27799381-e7da44ef-fc15-4bfd-923b-ba4a9de6b76a) |
| [List Company Time Off Reasons](actions/list-company-time-off-reasons.md) | `GET /company_timeoff_reasons` | [docs](https://www.postman.com/myhr-api/request/27799381-4ec08ae3-dd3a-4063-bb2e-65cdc06c3620) |
| [List Employee Addresses](actions/list-employee-addresses.md) | `GET /hr/employees/:employee_pid/addresses` | [docs](https://www.postman.com/myhr-api/request/27799381-75480e3e-a6fb-4091-925f-958cfb9d51a7) |
| [List Employee Assets For Employee](actions/list-employee-assets-for-employee.md) | `GET /employees/:employee_pid/employee_assets` | [docs](https://www.postman.com/myhr-api/request/27799381-8009cfa9-450c-46a4-9ee6-53bda237108c) |
| [List Employee Bonuses For Employee](actions/list-employee-bonuses-for-employee.md) | `GET /employees/:employee_pid/employee_bonuses` | [docs](https://www.postman.com/myhr-api/request/27799381-907b1100-8632-4091-b291-92ee8c39b299) |
| [List Employee Compensations For Employee](actions/list-employee-compensations-for-employee.md) | `GET /employees/:employee_pid/employee_compensations` | [docs](https://www.postman.com/myhr-api/request/27799381-68a7be88-7c14-4ba3-aab5-9739fcfea2a1) |
| [List Employee Expense Notes](actions/list-employee-expense-notes.md) | `GET /employee_expense_notes` | [docs](https://www.postman.com/myhr-api/request/27799381-21c474fc-c36b-4caf-93ed-fef0438a2ac5) |
| [List Employee Skills For Employee](actions/list-employee-skills-for-employee.md) | `GET /employees/:employee_pid/employee_skills` | [docs](https://www.postman.com/myhr-api/request/27799381-b68a9ce5-2c6f-4820-9ebe-c222b589f26a) |
| [List Employee Statuses](actions/list-employee-statuses.md) | `GET /hr/employees/:employee_pid/statuses` | [docs](https://www.postman.com/myhr-api/request/27799381-5f80f4d8-e644-4ca0-b838-5318c7624333) |
| [List Employee Time Off Request Days](actions/list-employee-time-off-request-days.md) | `GET /employee_timeoff_request_days` | [docs](https://www.postman.com/myhr-api/request/27799381-37f175cd-2b95-412f-9a7d-8d3cb61a7d58) |
| [List Employee Time Off Requests](actions/list-employee-time-off-requests.md) | `GET /employee_timeoff_requests` | [docs](https://www.postman.com/myhr-api/request/27799381-4402da2e-72bf-44b1-82ab-f8d5a92242df) |
| [List Employee Time Off Requests For Employee](actions/list-employee-time-off-requests-for-employee.md) | `GET /employees/:employee_pid/employee_timeoff_requests` | [docs](https://www.postman.com/myhr-api/request/27799381-a679c7bb-278a-4ad5-9d65-935532c54f9b) |
| [List Employee Training Courses For Employee](actions/list-employee-training-courses-for-employee.md) | `GET /employees/:employee_pid/employee_training_courses` | [docs](https://www.postman.com/myhr-api/request/27799381-d34ca02f-ef1c-4d85-abaa-27c958917ffb) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://www.postman.com/myhr-api/request/27799381-41dded66-442f-442e-956b-c609dfce9a83) |
| [List Employment Statuses](actions/list-employment-statuses.md) | `GET /cfg_employment_statuses` | [docs](https://www.postman.com/myhr-api/request/27799381-2ed3b5c3-32c8-4024-995c-455ce140236e) |
| [List Expense Note Expenses For Expense Note](actions/list-expense-note-expenses-for-expense-note.md) | `GET /employee_expense_notes/:employee_expense_note_pid/employee_expense_note_expenses` | [docs](https://www.postman.com/myhr-api/request/27799381-c12795b4-22f6-4aa3-90a5-e89baa129eed) |
| [List Punch Clock Clockins](actions/list-punch-clock-clockins.md) | `GET /analytics/punch-clock/clockins` | [docs](https://www.postman.com/myhr-api/request/27799381-a8ebe941-132a-473e-ab2b-b830fb7aa2a7) |
| [List Time Off Request Days For Employee](actions/list-time-off-request-days-for-employee.md) | `GET /employees/:employee_pid/employee_timeoff_request_days` | [docs](https://www.postman.com/myhr-api/request/27799381-584ec60a-e7ad-4d34-b30a-12a55f1d225a) |
| [List Time Off Request Days For Request](actions/list-time-off-request-days-for-request.md) | `GET /employee_timeoff_requests/:employee_timeoff_request_pid/employee_timeoff_request_days` | [docs](https://www.postman.com/myhr-api/request/27799381-01b0fef8-cf43-4cf1-adc0-f85b99b2867a) |
| [Move Employee Time Off Request To Trashbox](actions/move-employee-time-off-request-to-trashbox.md) | `DELETE /employee_timeoff_requests/:employee_timeoff_request_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-421c0011-9827-4d04-9049-819e7b1a0cfc) |
| [Terminate Employee](actions/terminate-employee.md) | `POST /hr/employees/:employee_pid/statuses/do/terminate` | [docs](https://www.postman.com/myhr-api/request/27799381-bf72dd47-8c68-45ea-844c-b82d8a0f418d) |
| [Update Company Time Off Reason](actions/update-company-time-off-reason.md) | `PUT /company_timeoff_reasons/:company_timeoff_reason_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-230f8f8b-2eff-4b54-a5dd-3b7a783a5ca4) |
| [Update Employee](actions/update-employee.md) | `PUT /employees/:employee_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-37025b1d-f6d9-405d-8071-dc99a24feb86) |
| [Update Employee Address](actions/update-employee-address.md) | `PATCH /hr/employees/:employee_pid/addresses/:employee_address_pid` | [docs](https://www.postman.com/myhr-api/request/27799381-49d25de7-6945-4854-8731-a71d65269ac9) |
| [Update Employee Time Off Request Status](actions/update-employee-time-off-request-status.md) | `PUT /employee_timeoff_requests/:employee_timeoff_request_pid/status` | [docs](https://www.postman.com/myhr-api/request/27799381-0b37fc72-1f8f-47d8-8e35-4a0c1b1dcff9) |
