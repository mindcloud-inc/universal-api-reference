# <img src="https://images.mindcloud.co/apps/icons/c-ats_1774548769491.png" alt="CATS logo" width="28" height="28"> CATS: Universal API

Manage recruiting pipelines, candidates, jobs, and hiring workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cATS/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://catsone.com/
- **Vendor API docs:** https://docs.catsone.com/api/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site](actions/get-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Candidate Activity](actions/create-candidate-activity.md) | POST | Creates a candidate activity in CATS. |
| [List Candidate Activities](actions/list-candidate-activities.md) | GET | Retrieves activities for a candidate in CATS. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Create Candidate](actions/create-candidate.md) | POST | Creates a new candidate in CATS. |
| [Delete Candidate](actions/delete-candidate.md) | DELETE | Deletes an existing candidate from CATS. |
| [Filter Candidates](actions/filter-candidates.md) | GET | Finds candidates in CATS by filter criteria. |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves details for a candidate in CATS. |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves candidates from the CATS account. |
| [Search Candidates](actions/search-candidates.md) | GET | Finds candidates in CATS by search query. |
| [Update Candidate](actions/update-candidate.md) | PUT | Updates an existing candidate in CATS. |

### Candidate Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate Application](actions/get-candidate-application.md) | GET | Retrieves a candidate application from CATS. |
| [List Applications By Candidate](actions/list-applications-by-candidate.md) | GET | Retrieves applications for a candidate in CATS. |

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [Upload Resume](actions/upload-resume.md) | PUT | Uploads a resume for a candidate in CATS. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in CATS. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from CATS. |
| [Get Company](actions/get-company.md) | GET | Retrieves details for a company in CATS. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from the CATS account. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in CATS by search query. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in CATS. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in CATS. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from CATS. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves details for a contact in CATS. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from the CATS account. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in CATS by search query. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in CATS. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Change Job Status](actions/change-job-status.md) | PUT | Updates the status of a job in CATS. |
| [Create Job](actions/create-job.md) | POST | Creates a new job in CATS. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing job from CATS. |
| [Filter Jobs](actions/filter-jobs.md) | GET | Finds jobs in CATS by filter criteria. |
| [Get Job](actions/get-job.md) | GET | Retrieves details for a job in CATS. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from the CATS account. |
| [Search Jobs](actions/search-jobs.md) | GET | Finds jobs in CATS by search query. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in CATS. |

### Job Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Application](actions/get-job-application.md) | GET | Retrieves a job application from CATS. |
| [List Applications By Job](actions/list-applications-by-job.md) | GET | Retrieves applications for a job in CATS. |

### Job Status

| Action | Method | Description |
| --- | --- | --- |
| [List Job Statuses](actions/list-job-statuses.md) | GET | Retrieves available job statuses from CATS. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Change Pipeline Status](actions/change-pipeline-status.md) | PUT | Updates the status of a pipeline in CATS. |
| [Create Pipeline](actions/create-pipeline.md) | POST | Creates a new pipeline in CATS. |
| [Delete Pipeline](actions/delete-pipeline.md) | DELETE | Deletes an existing pipeline from CATS. |
| [Filter Pipelines](actions/filter-pipelines.md) | GET | Finds pipelines in CATS by filter criteria. |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves details for a pipeline in CATS. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from the CATS account. |
| [List Pipelines By Candidate](actions/list-pipelines-by-candidate.md) | GET | Retrieves pipelines for a candidate in CATS. |
| [Update Pipeline](actions/update-pipeline.md) | PUT | Updates an existing pipeline in CATS. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves site details from the CATS account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from the CATS account. |

