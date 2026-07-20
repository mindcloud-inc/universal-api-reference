# <img src="https://images.mindcloud.co/apps/icons/gamalogic-icon_1776717803325.png" alt="Gamalogic logo" width="28" height="28"> Gamalogic: Universal API

Gamalogic provides REST APIs for real-time email verification, batch email validation, email discovery, and credit balance checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gamalogic/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gamalogic.com/
- **Vendor API docs:** https://docs.gamalogic.com/documentation/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Download Batch Result](actions/download-batch-result.md) | GET |  |
| [Find Email](actions/find-email.md) | GET |  |
| [Verify Email](actions/verify-email.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Status](actions/get-batch-status.md) | GET |  |
| [Verify Batch Emails](actions/verify-batch-emails.md) | POST |  |

