# <img src="https://images.mindcloud.co/apps/icons/mailcheck-icon_1775584690193.png" alt="Mailcheck logo" width="28" height="28"> Mailcheck: Universal API

Verify email deliverability, run bulk email checks, analyze email authenticity, rotate MailCheck API keys, and inspect MailCheck account usage from the MailCheck API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailcheck/latest
- **Category:** Communication / Email Communications
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailcheck.dev
- **Vendor API docs:** https://api.mailcheck.dev/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Rotate API Key](actions/rotate-api-key.md) | PUT |  |

### Authenticity Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email Authenticity](actions/verify-email-authenticity.md) | POST |  |
| [Verify Raw Email Authenticity](actions/verify-raw-email-authenticity.md) | POST |  |

### Bulk Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Verify Emails](actions/bulk-verify-emails.md) | POST |  |

### Email Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | POST |  |

