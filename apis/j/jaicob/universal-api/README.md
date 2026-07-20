# <img src="https://images.mindcloud.co/apps/icons/jaicob_1774554051746.png" alt="Jaicob logo" width="28" height="28"> Jaicob: Universal API

Manage candidates, applications, vacancies, clients, and locations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jaicob/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jaicob.ai
- **Vendor API docs:** https://developers.jaicob.ai/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Candidates](actions/list-candidates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST |  |
| [List Applications](actions/list-applications.md) | GET |  |
| [Retrieve Application](actions/retrieve-application.md) | GET |  |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Create Candidate](actions/create-candidate.md) | POST |  |
| [List Candidates](actions/list-candidates.md) | GET |  |
| [Retrieve Candidate](actions/retrieve-candidate.md) | GET |  |
| [Update Candidate](actions/update-candidate.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Retrieve Client](actions/retrieve-client.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Parse Resume](actions/parse-resume.md) | GET |  |

### Education

| Action | Method | Description |
| --- | --- | --- |
| [List Educations](actions/list-educations.md) | GET |  |

### Industry

| Action | Method | Description |
| --- | --- | --- |
| [List Industries](actions/list-industries.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Vacancy](actions/create-vacancy.md) | POST |  |
| [List Vacancies](actions/list-vacancies.md) | GET |  |
| [Retrieve Vacancy](actions/retrieve-vacancy.md) | GET |  |
| [Update Vacancy](actions/update-vacancy.md) | PUT |  |

### Job Category

| Action | Method | Description |
| --- | --- | --- |
| [List Job Categories](actions/list-job-categories.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Retrieve Location](actions/retrieve-location.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Seniority

| Action | Method | Description |
| --- | --- | --- |
| [List Seniorities](actions/list-seniorities.md) | GET |  |

