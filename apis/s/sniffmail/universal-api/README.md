# <img src="https://images.mindcloud.co/apps/icons/favicon-26_1777309392735.png" alt="Sniffmail logo" width="28" height="28"> Sniffmail: Universal API

Verify email addresses, detect disposable inboxes, and improve sender deliverability with Sniffmail's email verification API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sniffmail/latest
- **Category:** Communication / Email Communications
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sniffmail.io/
- **Vendor API docs:** https://sniffmail.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Credentials](actions/validate-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Bulk Job Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Results](actions/get-job-results.md) | GET | Retrieves results for a bulk verification job. |

### Bulk Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Job](actions/create-bulk-job.md) | POST | Creates a bulk email verification job in Sniffmail. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves the status of a bulk verification job. |

### Connection Test

| Action | Method | Description |
| --- | --- | --- |
| [Validate Credentials](actions/validate-credentials.md) | GET | Validates Sniffmail credentials with a test email verification request. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves email verification results from Sniffmail. |

