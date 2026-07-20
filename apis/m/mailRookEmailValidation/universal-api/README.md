# <img src="https://images.mindcloud.co/apps/icons/mailrook-icon-192_1775680974383.png" alt="MailRook Email Validation logo" width="28" height="28"> MailRook Email Validation: Universal API

Validate and enrich email addresses and domains with MailRook's email validation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailRookEmailValidation/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailrook.com
- **Vendor API docs:** https://mailrook.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Email](actions/validate-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Domain Enrichment

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Domain](actions/enrich-domain.md) | GET | Retrieves enrichment data from MailRook for a domain. |

### Domain Validation

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Input](actions/enrich-input.md) | GET | Retrieves enrichment data from MailRook for an email or domain. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address in MailRook. |

### Email Enrichment

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Email](actions/enrich-email.md) | GET | Retrieves enrichment data from MailRook for an email address. |

### Validation Batch

| Action | Method | Description |
| --- | --- | --- |
| [Submit Validation Batch](actions/submit-validation-batch.md) | POST | Submits a batch of email addresses for validation in MailRook. |

### Validation Batch Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Batch Results](actions/get-validation-batch-results.md) | GET | Retrieves email validation batch results from MailRook. |

