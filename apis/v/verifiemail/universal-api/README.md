# <img src="https://images.mindcloud.co/apps/icons/verifiemail_1774871267128.png" alt="verifi.email logo" width="28" height="28"> verifi.email: Universal API

Validate email addresses and check email-authentication domain health with the verifi.email API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verifiemail/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://verifi.email
- **Vendor API docs:** https://verifi.email/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Email](actions/validate-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Bulk Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Validate Emails](actions/bulk-validate-emails.md) | GET | Retrieves bulk email validation results from verifi.email using a JSON array. |
| [Bulk Validate Emails CSV](actions/bulk-validate-emails-csv.md) | GET | Retrieves bulk email validation results from verifi.email using the emails query parameter. |

### Domain Health

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain Health](actions/check-domain-health.md) | GET | Check a domain's email-authentication health and return SPF, DKIM, DMARC, and BIMI scores with recommendations. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validate a single email address and return deliverability checks, including syntax, MX, spoofing, and disposable-provider details. |

