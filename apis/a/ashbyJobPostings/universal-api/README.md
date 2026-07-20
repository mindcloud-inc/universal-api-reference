# <img src="https://images.mindcloud.co/apps/icons/ashby-app-icon_1776264523733.png" alt="Ashby Job Postings logo" width="28" height="28"> Ashby Job Postings: Universal API

Ashby job postings and custom careers-page wrapper covering public job board reads plus authenticated job posting, application, and survey flows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ashbyJobPostings/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ashbyhq.com
- **Vendor API docs:** https://developers.ashbyhq.com/docs/public-job-posting-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Published Job Postings](actions/list-published-job-postings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings?connectionId=$CONNECTION_ID&job_board_name=Ashby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Job Posting

| Action | Method | Description |
| --- | --- | --- |
| [List Published Job Postings](actions/list-published-job-postings.md) | GET | Retrieves published job postings from a specific Ashby job board. |

