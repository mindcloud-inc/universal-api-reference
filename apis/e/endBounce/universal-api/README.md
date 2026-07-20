# <img src="https://images.mindcloud.co/apps/icons/end-bounce_1775502860378.png" alt="EndBounce logo" width="28" height="28"> EndBounce: Universal API

Email verification and email finder API for validating addresses, running batch verification jobs, polling asynchronous verification jobs, and finding professional emails by name and domain.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/endBounce/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://endbounce.com
- **Vendor API docs:** https://app.endbounce.com/integrations

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Email](actions/find-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email?connectionId=$CONNECTION_ID&name=Ava%20Chen&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | GET | Finds an email in EndBounce by name and domain. |
| [Get Verification Job Results](actions/get-verification-job-results.md) | GET | Retrieves verification job results from EndBounce. |
| [Verify Email](actions/verify-email.md) | POST | Creates an email verification result in EndBounce. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Job Status](actions/get-verification-job-status.md) | GET | Retrieves a verification job status from EndBounce. |
| [Verify Emails Batch](actions/verify-emails-batch.md) | POST | Creates a verification job in EndBounce for multiple emails. |

