# TalentHR: Native API Reference

A consolidated summary of TalentHR's API configuration and 52 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.talenthr.io/
- **API base URL:** `https://pubapi.talenthr.io/v1`

## Authentication

### Basic

Use TalentHR Basic authentication. Enter your TalentHR API key as the username. The password may be left blank or set to any placeholder value.

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

[Official authentication documentation](https://help.talenthr.io/hc/en-us/articles/17627841146909-Can-I-integrate-my-site-app-or-custom-code-with-TalentHR-Do-you-offer-an-API)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Only one sort field is accepted.

## Endpoints (52 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Benefit Category](actions/create-benefit-category.md) | `POST /benefit-categories` | [docs](https://apidocs.talenthr.io/#a822d72d-d322-4376-b2e2-be3c0e649f08) |
| [Create Division](actions/create-division.md) | `POST /divisions` | [docs](https://apidocs.talenthr.io/#0a946c7e-91d6-4d9e-9012-27eebbcbc920) |
| [Create Holiday](actions/create-holiday.md) | `POST /holidays` | [docs](https://apidocs.talenthr.io/#b837d318-676b-4647-87a0-369c0870206a) |
| [Create Job Title](actions/create-job-title.md) | `POST /job-titles` | [docs](https://apidocs.talenthr.io/#35b2c197-6086-4711-b067-dbcd01238028) |
| [Create Location](actions/create-location.md) | `POST /locations` | [docs](https://apidocs.talenthr.io/#44d36dd5-8845-4098-957e-c79ce5d12ff0) |
| [Create Time Off Blocked Period](actions/create-time-off-blocked-period.md) | `POST /blocked-time-offs` | [docs](https://apidocs.talenthr.io/#74189047-c354-4de8-b879-bcb08e2f03cd) |
| [Create Time Off Type](actions/create-time-off-type.md) | `POST /time-off-types` | [docs](https://apidocs.talenthr.io/#6dca8ffd-4996-425e-b492-04931e57b7bc) |
| [Get Applicant](actions/get-applicant.md) | `GET /ats-applicants/:objectId` | [docs](https://apidocs.talenthr.io/#833a9f06-2343-4d29-b684-3c54ec780a96) |
| [Get Benefit Filters](actions/get-benefit-filters.md) | `GET /benefits/filters` | [docs](https://apidocs.talenthr.io/#7ae15e7f-674f-463c-ae36-a264a770c0da) |
| [Get Directory](actions/get-directory.md) | `GET /directory` | [docs](https://apidocs.talenthr.io/#7d5408ba-aa8b-4187-bd0e-0e347cdea5d0) |
| [Get Directory Filters](actions/get-directory-filters.md) | `GET /directory/filters` | [docs](https://apidocs.talenthr.io/#b25229d2-06f8-45f9-8b23-f14b725b7b77) |
| [Get Employee](actions/get-employee.md) | `GET /employees/:employee` | [docs](https://apidocs.talenthr.io/#43259b6a-44be-49ee-bd12-340bccd764a9) |
| [Get Employee Job Info](actions/get-employee-job-info.md) | `GET /employees/:employee/job` | [docs](https://apidocs.talenthr.io/#8b799f5a-3bf1-49de-9596-7c93bb9a0ab1) |
| [Get Organization Chart](actions/get-organization-chart.md) | `GET /organization-chart` | [docs](https://apidocs.talenthr.io/#2670259b-e767-41ca-97f8-80abe78300a1) |
| [List Benefit Categories](actions/list-benefit-categories.md) | `GET /benefit-categories` | [docs](https://apidocs.talenthr.io/#dff603fa-31e5-4288-a452-3799b334e34e) |
| [List Benefits](actions/list-benefits.md) | `GET /benefits` | [docs](https://apidocs.talenthr.io/#228f8389-67b5-4cd7-a3a0-92f8f20c3ab0) |
| [List Candidates](actions/list-candidates.md) | `GET /ats-applicants` | [docs](https://apidocs.talenthr.io/#94264a53-3741-4608-9f3d-87682bb2ee42) |
| [List Company Documents](actions/list-company-documents.md) | `GET /documents/company-documents` | [docs](https://apidocs.talenthr.io/#d0c0cca0-e32d-4762-88ca-25e92e1121e3) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://apidocs.talenthr.io/#4d331fe9-9e9f-4c1e-b848-7e2076ac0189) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://apidocs.talenthr.io/#03ff1c3f-881b-4aae-bf22-b30cc5c270d3) |
| [List Divisions](actions/list-divisions.md) | `GET /divisions` | [docs](https://apidocs.talenthr.io/#c6ca23d7-8331-46d8-b78f-77fe3c36fd3d) |
| [List Education Levels](actions/list-education-levels.md) | `GET /education-levels` | [docs](https://apidocs.talenthr.io/#2cdcb373-f69a-41a5-81f2-c2d66426f3ed) |
| [List Employee Assets](actions/list-employee-assets.md) | `GET /employees/:employee/assets` | [docs](https://apidocs.talenthr.io/#02e7bc80-2b16-4278-be9e-325031754db8) |
| [List Employee Available Assets](actions/list-employee-available-assets.md) | `GET /employees/:employee/available-assets` | [docs](https://apidocs.talenthr.io/#50c4f9e6-398e-4476-93c5-539391a77282) |
| [List Employee Benefits](actions/list-employee-benefits.md) | `GET /employees/:employee/benefits` | [docs](https://apidocs.talenthr.io/#829206cf-5527-4408-9c66-150ac04cb761) |
| [List Employee Completed Tasks](actions/list-employee-completed-tasks.md) | `GET /employees/:employee/tasks/completed` | [docs](https://apidocs.talenthr.io/#d548c77b-91eb-43ba-98bf-a04dfbb43e5d) |
| [List Employee Custom Fields](actions/list-employee-custom-fields.md) | `GET /employees/:employee/custom-fields` | [docs](https://apidocs.talenthr.io/#424e3e8c-37f6-4a41-b3a1-b279dbafc300) |
| [List Employee Documents](actions/list-employee-documents.md) | `GET /employees/:employee/documents` | [docs](https://apidocs.talenthr.io/#25efd277-dc78-4e91-87e5-6110a9ad2afe) |
| [List Employee Managers](actions/list-employee-managers.md) | `GET /employees/:employee/managers` | [docs](https://apidocs.talenthr.io/#e8816c2b-22f2-4a0e-b329-aa841d42261c) |
| [List Employee Pending Tasks](actions/list-employee-pending-tasks.md) | `GET /employees/:employee/tasks/pending` | [docs](https://apidocs.talenthr.io/#e90d17c5-0e6b-47ad-b69b-96048515126d) |
| [List Employee Time Off Budgets](actions/list-employee-time-off-budgets.md) | `GET /employees/:employee/time-off-budgets` | [docs](https://apidocs.talenthr.io/#91964ca0-2bd4-46f1-ae78-8c7c6a838321) |
| [List Employee Time Off Requests](actions/list-employee-time-off-requests.md) | `GET /employees/:employee/time-off-requests` | [docs](https://apidocs.talenthr.io/#a084bf09-87f6-4c1f-86d0-2d42f5944f35) |
| [List Employment Statuses](actions/list-employment-statuses.md) | `GET /employment-statuses` | [docs](https://apidocs.talenthr.io/#58f66d30-ca8d-48b2-8962-1ad848de4537) |
| [List Holiday Years](actions/list-holiday-years.md) | `GET /holidays/years` | [docs](https://apidocs.talenthr.io/#fd12071f-cadc-4fd8-ba89-e67827342ec2) |
| [List Holidays](actions/list-holidays.md) | `GET /holidays` | [docs](https://apidocs.talenthr.io/#b982bd62-450c-42ea-830d-baad9cdbc681) |
| [List Job Position Applicants](actions/list-job-position-applicants.md) | `GET /job-positions/:jobPosition/ats-applicants` | [docs](https://apidocs.talenthr.io/#aa58799a-5b48-43f2-9664-3ec0787083d9) |
| [List Job Positions](actions/list-job-positions.md) | `GET /job-positions` | [docs](https://apidocs.talenthr.io/#c5cf88f2-4733-42b3-9b85-bbde3ddb0bf2) |
| [List Job Titles](actions/list-job-titles.md) | `GET /job-titles` | [docs](https://apidocs.talenthr.io/#6626b153-e7fe-4a73-b90f-4c2a6b433327) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://apidocs.talenthr.io/#a7048895-91f1-459a-9bd3-45aa19463241) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://apidocs.talenthr.io/#4e880b05-33a5-48d9-969b-6b5ca001b925) |
| [List Nationalities](actions/list-nationalities.md) | `GET /nationalities` | [docs](https://apidocs.talenthr.io/#e3f3f91b-e2ff-43cc-a9ff-987951f1f92e) |
| [List Published Job Positions](actions/list-published-job-positions.md) | `GET /job-positions/published` | [docs](https://apidocs.talenthr.io/#68ed940e-2ea4-4416-9a35-503afc5bc3a1) |
| [List Relationship Types](actions/list-relationship-types.md) | `GET /relationship-types` | [docs](https://apidocs.talenthr.io/#536c78cc-71b3-42ca-8828-30c969f73898) |
| [List Time Off Blocked Periods](actions/list-time-off-blocked-periods.md) | `GET /blocked-time-offs` | [docs](https://apidocs.talenthr.io/#158f3ab3-0da9-426f-a826-611ec58d0113) |
| [List Time Off Types](actions/list-time-off-types.md) | `GET /time-off-types` | [docs](https://apidocs.talenthr.io/#e485e651-e54b-4c4f-9059-1214c5957be7) |
| [List Timezones](actions/list-timezones.md) | `GET /timezones` | [docs](https://apidocs.talenthr.io/#877ac170-e5c4-4aeb-b789-6eaa79eb1bb2) |
| [Update Benefit Category](actions/update-benefit-category.md) | `PUT /benefit-categories/:objectId` | [docs](https://apidocs.talenthr.io/#88073194-9944-40fd-839c-0a45f5609e0b) |
| [Update Division](actions/update-division.md) | `PUT /divisions/:objectId` | [docs](https://apidocs.talenthr.io/#aff24708-0102-4f32-b8f5-deccff71235b) |
| [Update Holiday](actions/update-holiday.md) | `PUT /holidays/:objectId` | [docs](https://apidocs.talenthr.io/#01e85519-8c14-42c5-b073-7f5fa46aa5e2) |
| [Update Job Title](actions/update-job-title.md) | `PUT /job-titles/:objectId` | [docs](https://apidocs.talenthr.io/#372cca97-bc1c-4b16-96b2-68837913b6d8) |
| [Update Location](actions/update-location.md) | `PUT /locations/:objectId` | [docs](https://apidocs.talenthr.io/#c517de21-64eb-479f-bb71-82d9a198a045) |
| [Update Time Off Blocked Period](actions/update-time-off-blocked-period.md) | `PUT /blocked-time-offs/:objectId` | [docs](https://apidocs.talenthr.io/#55e963ae-0331-4086-bd7a-972088c3a42c) |
