# <img src="https://images.mindcloud.co/apps/icons/hires-ats_1774549058671.png" alt="100Hires ATS logo" width="28" height="28"> 100Hires ATS: Universal API

Manage candidates, applications, jobs, forms, and recruiting workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hiresATS/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://100hires.com
- **Vendor API docs:** https://100hires.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Advance Application To Next Stage](actions/advance-application-to-next-stage.md) | PUT | Advances an application to the next stage in 100Hires ATS. |
| [Create Application](actions/create-application.md) | POST | Creates a new application in 100Hires ATS. |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from 100Hires ATS. |
| [Get Application AI Score](actions/get-application-ai-score.md) | GET | Retrieves an application's AI score from 100Hires ATS. |
| [List Applications](actions/list-applications.md) | GET | Lists the applications in 100Hires ATS. |
| [Mark Application As Hired](actions/mark-application-as-hired.md) | PUT | Marks an application as hired in 100Hires ATS. |
| [Move Application To Stage](actions/move-application-to-stage.md) | PUT | Moves an application to a stage in 100Hires ATS. |
| [Reject Application](actions/reject-application.md) | PUT | Rejects an application in 100Hires ATS. |
| [Transfer Application To Another Job](actions/transfer-application-to-another-job.md) | PUT | Transfers an application to another job in 100Hires ATS. |
| [Update Application](actions/update-application.md) | PUT | Updates an existing application in 100Hires ATS. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Batch Add Tags To Candidates](actions/batch-add-tags-to-candidates.md) | PUT | Adds tags to multiple candidates in 100Hires ATS. |
| [Batch Remove Tags From Candidates](actions/batch-remove-tags-from-candidates.md) | PUT | Removes tags from multiple candidates in 100Hires ATS. |
| [Create Candidate](actions/create-candidate.md) | POST | Creates a new candidate in 100Hires ATS. |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves a candidate from 100Hires ATS. |
| [List Candidates](actions/list-candidates.md) | GET | Lists the candidates in 100Hires ATS. |
| [Update Candidate](actions/update-candidate.md) | PUT | Updates an existing candidate in 100Hires ATS. |

### Candidate Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Candidate Activities](actions/list-candidate-activities.md) | GET | Lists a candidate's activities in 100Hires ATS. |

### Evaluation Form

| Action | Method | Description |
| --- | --- | --- |
| [List Application Evaluation Forms](actions/list-application-evaluation-forms.md) | GET | Lists filled evaluation forms for an application in 100Hires ATS. |

### Hiring Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Hiring Team Member](actions/add-hiring-team-member.md) | PUT | Adds a hiring team member to a job in 100Hires ATS. |
| [List Job Hiring Team](actions/list-job-hiring-team.md) | GET | Lists a job's hiring team in 100Hires ATS. |

### Interview

| Action | Method | Description |
| --- | --- | --- |
| [Create Interview](actions/create-interview.md) | POST | Schedules an interview for an application in 100Hires ATS. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in 100Hires ATS. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from 100Hires ATS. |
| [List Jobs](actions/list-jobs.md) | GET | Lists the jobs in 100Hires ATS. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in 100Hires ATS. |
| [Update Job Status](actions/update-job-status.md) | PUT | Updates a job's status in 100Hires ATS. |

### Mail Account

| Action | Method | Description |
| --- | --- | --- |
| [List User Mail Accounts](actions/list-user-mail-accounts.md) | GET | Lists a user's mail accounts in 100Hires ATS. |

### Rejection Reason

| Action | Method | Description |
| --- | --- | --- |
| [List Rejection Reasons](actions/list-rejection-reasons.md) | GET | Lists the rejection reasons in 100Hires ATS. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Company Tags](actions/list-company-tags.md) | GET | Lists the company tags in 100Hires ATS. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from 100Hires ATS. |
| [List Users](actions/list-users.md) | GET | Lists the users in 100Hires ATS. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Lists the workflows in 100Hires ATS. |

### Workflow Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Stages](actions/list-workflow-stages.md) | GET | Lists the workflow stages in 100Hires ATS. |

