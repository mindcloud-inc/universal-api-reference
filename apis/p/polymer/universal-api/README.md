# <img src="https://images.mindcloud.co/apps/icons/favicon-developer-polymer-co-48x48_1778268859979.png" alt="Polymer logo" width="28" height="28"> Polymer: Universal API

Polymer is an applicant tracking system API for managing organizations, hiring users, jobs, candidates, job applications, comments, reviews, hiring stages, and application messages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/polymer/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://polymer.co
- **Vendor API docs:** https://developer.polymer.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Candidate](actions/get-candidate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Active Users

| Action | Method | Description |
| --- | --- | --- |
| [List Active Users](actions/list-active-users.md) | GET | Retrieves active organization users from Polymer. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves a candidate from Polymer. |

### Candidate With Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate With Applications](actions/get-candidate-with-applications.md) | GET | Retrieves a candidate and job applications from Polymer. |

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves candidates from Polymer. |

### Deactivated Users

| Action | Method | Description |
| --- | --- | --- |
| [List Deactivated Users](actions/list-deactivated-users.md) | GET | Retrieves deactivated organization users from Polymer. |

### Hiring Stage Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Hiring Stage Events](actions/get-hiring-stage-events.md) | GET | Retrieves hiring stage events for a job application in Polymer. |

### Hiring Stages

| Action | Method | Description |
| --- | --- | --- |
| [Get Hiring Stages](actions/get-hiring-stages.md) | GET | Retrieves hiring stages for a job in Polymer. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Polymer. |

### Job Application

| Action | Method | Description |
| --- | --- | --- |
| [Apply For Job](actions/apply-for-job.md) | POST | Applies a candidate to a job in Polymer. |
| [Get Job Application](actions/get-job-application.md) | GET | Retrieves a job application from Polymer. |
| [Import Job Application](actions/import-job-application.md) | POST | Imports a job application into Polymer. |

### Job Application Archive

| Action | Method | Description |
| --- | --- | --- |
| [Archive Job Application](actions/archive-job-application.md) | PUT | Archives a job application in Polymer. |

### Job Application Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Application Comment](actions/create-job-application-comment.md) | POST | Creates a comment for a job application in Polymer. |
| [Delete Job Application Comment](actions/delete-job-application-comment.md) | DELETE | Deletes an existing job application comment from Polymer. |
| [Update Job Application Comment](actions/update-job-application-comment.md) | PUT | Updates an existing job application comment in Polymer. |

### Job Application Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Application Comments](actions/get-job-application-comments.md) | GET | Retrieves comments for a job application in Polymer. |

### Job Application Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Application Messages](actions/get-job-application-messages.md) | GET | Retrieves messages for a job application in Polymer. |

### Job Application Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Application Review](actions/create-job-application-review.md) | POST | Creates a review for a job application in Polymer. |
| [Delete Job Application Review](actions/delete-job-application-review.md) | DELETE | Deletes an existing job application review from Polymer. |
| [Update Job Application Review](actions/update-job-application-review.md) | PUT | Updates an existing job application review in Polymer. |

### Job Application Reviews

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Application Reviews](actions/get-job-application-reviews.md) | GET | Retrieves reviews for a job application in Polymer. |

### Job Application Stage

| Action | Method | Description |
| --- | --- | --- |
| [Move Job Application Stage](actions/move-job-application-stage.md) | PUT | Moves a job application to a hiring stage in Polymer. |

### Job Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Job Applications](actions/list-job-applications.md) | GET | Retrieves job applications from Polymer. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from Polymer. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves the current organization from Polymer. |

### Organization User

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization User](actions/get-organization-user.md) | GET | Retrieves an organization user from Polymer. |

### Resume Export Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Resume Export](actions/get-resume-export.md) | GET | Retrieves a resume export job from Polymer. |
| [Start Resume Export](actions/start-resume-export.md) | POST | Starts a resume export job in Polymer. |

