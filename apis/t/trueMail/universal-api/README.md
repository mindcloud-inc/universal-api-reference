# <img src="https://images.mindcloud.co/apps/icons/truemail-icon-square_1775668517731.png" alt="TrueMail logo" width="28" height="28"> TrueMail: Universal API

Verify email addresses, inspect usage, and manage MailCop filters from TrueMail.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trueMail/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailcop.net
- **Vendor API docs:** https://mailcop.net/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Usage](actions/check-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Validates an email address in TrueMail. |
| [Verify Email MX](actions/verify-email-mx.md) | GET | Validates an email address with MX checks in TrueMail. |
| [Verify Email SMTP](actions/verify-email-smtp.md) | GET | Validates an email address with SMTP checks in TrueMail. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Create Filter](actions/create-filter.md) | POST | Creates a new blocklist filter in TrueMail. |
| [Delete Filter](actions/delete-filter.md) | DELETE | Deletes an existing blocklist filter from TrueMail. |
| [List Domain Filters](actions/list-domain-filters.md) | GET | Retrieves saved domain filters from TrueMail. |
| [List Email Filters](actions/list-email-filters.md) | GET | Retrieves saved email filters from TrueMail. |
| [List Filters](actions/list-filters.md) | GET | Retrieves saved blocklist filters from TrueMail. |
| [List IP Filters](actions/list-ip-filters.md) | GET | Retrieves saved IP address filters from TrueMail. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Check Usage](actions/check-usage.md) | GET | Retrieves account usage details from TrueMail. |

