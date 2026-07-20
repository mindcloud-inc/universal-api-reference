# <img src="https://images.mindcloud.co/apps/icons/favicon-apidocs-jobsoid-com-48x48_1776802815822.png" alt="Jobsoid logo" width="28" height="28"> Jobsoid: Universal API

Source candidates, manage hiring pipelines, and publish jobs with Jobsoid

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jobsoid/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jobsoid.com/
- **Vendor API docs:** https://apidocs.jobsoid.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get job](actions/get-job.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=130458" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List departments](actions/list-departments.md) | GET | Retrieves departments from Jobsoid. |

### Divisions

| Action | Method | Description |
| --- | --- | --- |
| [List divisions](actions/list-divisions.md) | GET | Retrieves divisions from Jobsoid. |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [Get job](actions/get-job.md) | GET | Retrieves a published job from Jobsoid. |
| [List jobs](actions/list-jobs.md) | GET | Retrieves published jobs from Jobsoid. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List locations](actions/list-locations.md) | GET | Retrieves locations from Jobsoid. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List job functions](actions/list-job-functions.md) | GET | Retrieves job functions from Jobsoid. |

