# AssessTEAM: Native API Reference

A consolidated summary of AssessTEAM's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://restapi.assessteam.com/swagger/index.html
- **OpenAPI specification:** https://restapi.assessteam.com/swagger/v1/swagger.json
- **API base URL:** `https://restapi.assessteam.com`

## Authentication

### API Key Token Flow

Use an AssessTEAM API key and company name to mint a bearer token before running actions.

### Credentials

- **API Key:** `apiKey` · required · AssessTEAM API key from Settings -> Integrations -> Application Programming Interface.
- **Company Name:** `companyName` · required · AssessTEAM workspace subdomain / company name used by the token endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <custom.data.accesstoken>
```

[Official authentication documentation](https://restapi.assessteam.com/swagger/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Person](actions/add-person.md) | `POST /person/addperson` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Add Timesheet](actions/add-timesheet.md) | `POST /timesheet/addtimesheet` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Delete Person](actions/delete-person.md) | `POST /person/deleteperson` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Generate Access Token](actions/generate-access-token.md) | `POST /auth/generatetoken` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Get Person](actions/get-person.md) | `POST /person/getperson` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Get Timely Timesheet Data](actions/get-timely-timesheet-data.md) | `GET /timesheet/getTimelyTimesheetData` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Get Timesheet Data](actions/get-timesheet-data.md) | `GET /timesheet/gettimesheetdata` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [List Evaluations Report](actions/list-evaluations-report.md) | `GET /reports/evaluations` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [List Performance Indicators Report](actions/list-performance-indicators-report.md) | `GET /reports/performanceindicators` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [List Persons Report](actions/list-persons-report.md) | `GET /reports/persons` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [List Result Areas Report](actions/list-result-areas-report.md) | `GET /reports/resultareas` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [List Teams](actions/list-teams.md) | `GET /reports/teams` | [docs](https://restapi.assessteam.com/swagger/index.html) |
| [Update Person](actions/update-person.md) | `POST /person/updateperson` | [docs](https://restapi.assessteam.com/swagger/index.html) |
