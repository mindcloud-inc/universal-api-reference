# <img src="https://images.mindcloud.co/apps/icons/findy-mail_1776107834615.png" alt="FindyMail logo" width="28" height="28"> FindyMail: Universal API

FindyMail provides B2B data enrichment APIs for finding verified work emails, verifying email deliverability, finding phone numbers, enriching companies, finding employees, and reverse email lookup.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/findyMail/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.findymail.com
- **Vendor API docs:** https://www.findymail.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email](actions/verify-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves company enrichment data from FindyMail. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | GET | Finds a verified email in FindyMail. |
| [Find People](actions/find-people.md) | GET | Finds people in FindyMail. |
| [Find Phone Number](actions/find-phone-number.md) | GET | Finds a phone number in FindyMail. |
| [Reverse Email Lookup](actions/reverse-email-lookup.md) | GET | Finds contact details in FindyMail by email address. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address with FindyMail. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Start Lead Search](actions/start-lead-search.md) | GET | Starts a lead search in FindyMail. |

