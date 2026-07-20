# <img src="https://images.mindcloud.co/apps/icons/assess-team_1775502377851.png" alt="AssessTEAM logo" width="28" height="28"> AssessTEAM: Universal API

Manage employee evaluations, goals, OKRs, and performance reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assessTEAM/latest
- **Category:** Human Resources / HRIS
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assessteam.com/
- **Vendor API docs:** https://restapi.assessteam.com/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate Access Token](actions/generate-access-token.md) | GET | Retrieves an access token from AssessTEAM. |

### Evaluations Report

| Action | Method | Description |
| --- | --- | --- |
| [List Evaluations Report](actions/list-evaluations-report.md) | GET | Retrieves the evaluations report from AssessTEAM. |

### Performance Indicators Report

| Action | Method | Description |
| --- | --- | --- |
| [List Performance Indicators Report](actions/list-performance-indicators-report.md) | GET | Retrieves the performance indicators report from AssessTEAM. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Add Person](actions/add-person.md) | POST | Creates a new person in AssessTEAM. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from AssessTEAM. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person by person code from AssessTEAM. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in AssessTEAM. |

### Persons Report

| Action | Method | Description |
| --- | --- | --- |
| [List Persons Report](actions/list-persons-report.md) | GET | Retrieves the persons report from AssessTEAM. |

### Result Areas Report

| Action | Method | Description |
| --- | --- | --- |
| [List Result Areas Report](actions/list-result-areas-report.md) | GET | Retrieves the result areas report from AssessTEAM. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves the teams report from AssessTEAM. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Add Timesheet](actions/add-timesheet.md) | POST | Creates a new timesheet entry in AssessTEAM. |
| [Get Timely Timesheet Data](actions/get-timely-timesheet-data.md) | GET | Retrieves timely timesheet data from AssessTEAM. |
| [Get Timesheet Data](actions/get-timesheet-data.md) | GET | Retrieves recorded timesheet data from AssessTEAM. |

