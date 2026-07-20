# <img src="https://images.mindcloud.co/apps/icons/224067_1775159079116.png" alt="MailFloss logo" width="28" height="28"> MailFloss: Universal API

Verify emails, manage deletion requests, and update integration settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailFloss/latest
- **Category:** Communication / Email Communications
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailfloss.com
- **Vendor API docs:** https://developers.mailfloss.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email Address](actions/verify-email-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Delete Emails](actions/delete-emails.md) | DELETE | Deletes email addresses from MailFloss privacy storage. |
| [Get Batch Verification Results](actions/get-batch-verification-results.md) | GET | Retrieves batch email verification results from MailFloss. |
| [Verify Email Address](actions/verify-email-address.md) | GET | Verifies an email address with MailFloss. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Change Integration Setting](actions/change-integration-setting.md) | PUT | Updates an integration setting in MailFloss. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch Verification Job](actions/cancel-batch-verification-job.md) | PUT | Cancels a batch email verification job in MailFloss. |
| [Create Batch Verification Job](actions/create-batch-verification-job.md) | POST | Creates a batch email verification job in MailFloss. |
| [Get Batch Verification Status](actions/get-batch-verification-status.md) | GET | Retrieves batch email verification job status from MailFloss. |

