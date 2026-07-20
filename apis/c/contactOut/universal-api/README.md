# <img src="https://images.mindcloud.co/apps/icons/contact-out_1774621901959.png" alt="ContactOut logo" width="28" height="28"> ContactOut: Universal API

ContactOut provides people, company, and email intelligence APIs for profile enrichment, search, and contact verification.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contactOut/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contactout.com
- **Vendor API docs:** https://api.contactout.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Usage Stats](actions/get-api-usage-stats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Domain](actions/enrich-domain.md) | GET | Retrieves company details for domain names in ContactOut. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in ContactOut using company search filters. |
| [Search Companies HQ Only](actions/search-companies-hq-only.md) | GET | Finds HQ-only companies in ContactOut using company search filters. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Batch Get LinkedIn Contact Info](actions/batch-get-linked-in-contact-info.md) | GET | Retrieves contact details for LinkedIn profiles in bulk from ContactOut. |
| [Check Personal Email Status](actions/check-personal-email-status.md) | GET | Retrieves personal email availability for a LinkedIn profile in ContactOut. |
| [Check Phone Status](actions/check-phone-status.md) | GET | Retrieves phone availability for a LinkedIn profile in ContactOut. |
| [Check Work Email Status](actions/check-work-email-status.md) | GET | Retrieves work email availability for a LinkedIn profile in ContactOut. |
| [Count People](actions/count-people.md) | GET | Retrieves a count of people matching search filters in ContactOut. |
| [Enrich Email](actions/enrich-email.md) | GET | Retrieves profile details from an email address in ContactOut. |
| [Enrich Email With Work Email](actions/enrich-email-with-work-email.md) | GET | Retrieves profile details and work email from ContactOut. |
| [Enrich LinkedIn Profile](actions/enrich-linked-in-profile.md) | GET | Retrieves profile details from a LinkedIn URL in ContactOut. |
| [Enrich Person](actions/enrich-person.md) | GET | Retrieves a person's profile from ContactOut using multiple identifiers. |
| [Enrich Person With Personal Email](actions/enrich-person-with-personal-email.md) | GET | Retrieves a person's profile and personal email from ContactOut. |
| [Enrich Person With Phone](actions/enrich-person-with-phone.md) | GET | Retrieves a person's profile and phone from ContactOut. |
| [Enrich Person With Work Email](actions/enrich-person-with-work-email.md) | GET | Retrieves a person's profile and work email from ContactOut. |
| [Get Decision Makers By Company Name](actions/get-decision-makers-by-company-name.md) | GET | Retrieves decision makers by company name from ContactOut. |
| [Get Decision Makers By Domain](actions/get-decision-makers-by-domain.md) | GET | Retrieves decision makers by company domain from ContactOut. |
| [Get Decision Makers By LinkedIn Company URL](actions/get-decision-makers-by-linked-in-company-url.md) | GET | Retrieves decision makers by LinkedIn company URL from ContactOut. |
| [Get Decision Makers With Contact Reveal](actions/get-decision-makers-with-contact-reveal.md) | GET | Retrieves decision makers with revealed contact information from ContactOut. |
| [Get LinkedIn Contact Info](actions/get-linked-in-contact-info.md) | GET | Retrieves contact details for a LinkedIn profile from ContactOut. |
| [Get LinkedIn Contact Info With Phone](actions/get-linked-in-contact-info-with-phone.md) | GET | Retrieves contact details and phone for a LinkedIn profile from ContactOut. |
| [Get Person By Email](actions/get-person-by-email.md) | GET | Retrieves a LinkedIn profile from an email address in ContactOut. |
| [Search People](actions/search-people.md) | GET | Finds people in ContactOut using people search filters. |
| [Search People By Company](actions/search-people-by-company.md) | GET | Finds people in ContactOut by company. |
| [Search People By Job Title](actions/search-people-by-job-title.md) | GET | Finds people in ContactOut by job title. |
| [Search People With Contact Reveal](actions/search-people-with-contact-reveal.md) | GET | Finds people in ContactOut with revealed contact information. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves an email verification result from ContactOut. |

### Email Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Email Verification Job](actions/get-batch-email-verification-job.md) | GET | Retrieves a batch email verification job from ContactOut. |
| [Queue Batch Email Verification](actions/queue-batch-email-verification.md) | POST | Creates a batch email verification job in ContactOut. |

### Usage Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get API Usage Stats](actions/get-api-usage-stats.md) | GET | Retrieves API usage stats for a month in ContactOut. |

