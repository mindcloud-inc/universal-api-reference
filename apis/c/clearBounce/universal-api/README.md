# <img src="https://images.mindcloud.co/apps/icons/favicon-32_1775696699409.png" alt="ClearBounce logo" width="28" height="28"> ClearBounce: Universal API

ClearBounce email verification and deliverability API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clearBounce/latest
- **Category:** Communication / Email Communications
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clearbounce.net/
- **Vendor API docs:** https://docs.clearbounce.net/api-reference/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Batch Verification Job](actions/get-batch-verification-job.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Verification Job](actions/create-batch-verification-job.md) | POST | Creates a batch verification job in ClearBounce. |
| [Get Batch Verification Job](actions/get-batch-verification-job.md) | GET | Retrieves a batch verification job from ClearBounce. |
| [Get Batch Verification Results](actions/get-batch-verification-results.md) | GET | Retrieves JSON batch verification results from ClearBounce. |
| [Get Batch Verification Results Raw](actions/get-batch-verification-results-raw.md) | GET | Retrieves raw batch verification results from ClearBounce. |
| [Verify Email](actions/verify-email.md) | GET | Verifies a single email address in ClearBounce. |

