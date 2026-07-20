# <img src="https://images.mindcloud.co/apps/icons/never-bounce_1773414813766.png" alt="NeverBounce logo" width="28" height="28"> NeverBounce: Universal API

Verify email addresses, manage jobs, and download validation results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neverBounce/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://neverbounce.com
- **Vendor API docs:** https://developers.neverbounce.com/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details and usage information from NeverBounce. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address in NeverBounce. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job From Remote URL](actions/create-job-from-remote-url.md) | POST | Creates a verification job in NeverBounce from a remote CSV URL. |
| [Create Job From Supplied Data](actions/create-job-from-supplied-data.md) | POST | Creates a verification job in NeverBounce from supplied rows. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing verification job from NeverBounce. |
| [Download Job Results](actions/download-job-results.md) | GET | Retrieves downloadable job results from NeverBounce. |
| [Get Job Results](actions/get-job-results.md) | GET | Retrieves detailed job results from NeverBounce. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves the current status of a NeverBounce job. |
| [Parse Job](actions/parse-job.md) | PUT | Updates an existing NeverBounce job by parsing its uploaded data. |
| [Search Jobs](actions/search-jobs.md) | GET | Finds NeverBounce jobs by filter criteria. |
| [Start Job](actions/start-job.md) | PUT | Updates an existing NeverBounce job by starting verification. |

