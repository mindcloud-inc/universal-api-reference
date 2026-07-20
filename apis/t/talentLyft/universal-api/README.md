# <img src="https://images.mindcloud.co/apps/icons/cropped-favicon-5-32x32_1777051620793.png" alt="TalentLyft logo" width="28" height="28"> TalentLyft: Universal API

TalentLyft is recruiting software for sourcing candidates, managing jobs, forms, applications, and team members.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/talentLyft/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.talentlyft.com/
- **Vendor API docs:** https://developers.talentlyft.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST | Creates a new department in TalentLyft. |
| [Delete Department](actions/delete-department.md) | DELETE | Deletes an existing department from TalentLyft. |
| [Get Department](actions/get-department.md) | GET | Retrieves a department from TalentLyft. |
| [Get Department By External ID](actions/get-department-by-external-id.md) | GET | Retrieves a department in TalentLyft by external ID. |
| [Get Departments](actions/get-departments.md) | GET | Retrieves all departments from TalentLyft. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in TalentLyft. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employees](actions/get-employees.md) | GET | Retrieves all employees from TalentLyft. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Forms](actions/get-forms.md) | GET | Retrieves all forms from TalentLyft. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Jobs](actions/get-jobs.md) | GET | Retrieves all jobs from TalentLyft. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Get Articles](actions/get-articles.md) | GET | Retrieves all articles from TalentLyft. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Locations](actions/get-job-locations.md) | GET | Retrieves public job locations from TalentLyft. |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Get Meetings](actions/get-meetings.md) | GET | Retrieves all meetings from TalentLyft. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves all company members from TalentLyft. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from TalentLyft. |
| [Get Pipelines](actions/get-pipelines.md) | GET | Retrieves all pipelines from TalentLyft. |

### Rejection Reasons

| Action | Method | Description |
| --- | --- | --- |
| [Create Rejection Reason](actions/create-rejection-reason.md) | POST | Creates a new rejection reason in TalentLyft. |
| [Delete Rejection Reason](actions/delete-rejection-reason.md) | DELETE | Deletes an existing rejection reason from TalentLyft. |
| [Get Rejection Reason](actions/get-rejection-reason.md) | GET | Retrieves a rejection reason from TalentLyft. |
| [Get Rejection Reasons](actions/get-rejection-reasons.md) | GET | Retrieves rejection reasons from TalentLyft. |
| [Update Rejection Reason](actions/update-rejection-reason.md) | PUT | Updates an existing rejection reason in TalentLyft. |

