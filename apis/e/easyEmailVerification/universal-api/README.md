# <img src="https://images.mindcloud.co/apps/icons/easy-email-verification_1774383355243.png" alt="Easy Email Verification logo" width="28" height="28"> Easy Email Verification: Universal API

Verify emails and manage bulk verification jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyEmailVerification/latest
- **Category:** Communication / Email Communications
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easyemailverification.com
- **Vendor API docs:** https://eev.stoplight.io/docs/eev/902yv4tm9bfd9-easy-email-verification-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bulk Jobs](actions/list-bulk-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Bulk Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Bulk Verification Job](actions/delete-bulk-verification-job.md) | DELETE | Deletes a bulk verification job from Easy Email Verification. |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | GET | Retrieves a bulk job status from Easy Email Verification. |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | GET | Retrieves all bulk job statuses from Easy Email Verification. |
| [Upload Bulk Email File](actions/upload-bulk-email-file.md) | POST | Creates a bulk verification job in Easy Email Verification. |

### Bulk Result File

| Action | Method | Description |
| --- | --- | --- |
| [Download Processed Results File](actions/download-processed-results-file.md) | GET | Retrieves a processed bulk results file from Easy Email Verification. |

### Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves an email verification result from Easy Email Verification. |
| [Verify Email List](actions/verify-email-list.md) | GET | Retrieves verification results for up to 50 emails in Easy Email Verification. |

