# ContactOut: Native API Reference

A consolidated summary of ContactOut's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.contactout.com/
- **API base URL:** `https://api.contactout.com`

## Authentication

### API Key

Use a ContactOut API key passed in the token request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://api.contactout.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Get LinkedIn Contact Info](actions/batch-get-linked-in-contact-info.md) | `POST /v1/people/linkedin/batch` | [docs](https://api.contactout.com/#v1-bulk-contactinfo) |
| [Check Personal Email Status](actions/check-personal-email-status.md) | `GET /v1/people/linkedin/personal_email_status` | [docs](https://api.contactout.com/#personal-email-checker) |
| [Check Phone Status](actions/check-phone-status.md) | `GET /v1/people/linkedin/phone_status` | [docs](https://api.contactout.com/#phone-number-checker) |
| [Check Work Email Status](actions/check-work-email-status.md) | `GET /v1/people/linkedin/work_email_status` | [docs](https://api.contactout.com/#work-email-checker) |
| [Count People](actions/count-people.md) | `POST /v1/people/count` | [docs](https://api.contactout.com/#people-count-api) |
| [Enrich Domain](actions/enrich-domain.md) | `POST /v1/domain/enrich` | [docs](https://api.contactout.com/#company-information-from-domains) |
| [Enrich Email](actions/enrich-email.md) | `GET /v1/email/enrich` | [docs](https://api.contactout.com/#from-email-address) |
| [Enrich Email With Work Email](actions/enrich-email-with-work-email.md) | `GET /v1/email/enrich` | [docs](https://api.contactout.com/#from-email-address) |
| [Enrich LinkedIn Profile](actions/enrich-linked-in-profile.md) | `GET /v1/linkedin/enrich` | [docs](https://api.contactout.com/#from-linkedin-url) |
| [Enrich Person](actions/enrich-person.md) | `POST /v1/people/enrich` | [docs](https://api.contactout.com/#people-enrich-api) |
| [Enrich Person With Personal Email](actions/enrich-person-with-personal-email.md) | `POST /v1/people/enrich` | [docs](https://api.contactout.com/#people-enrich-api) |
| [Enrich Person With Phone](actions/enrich-person-with-phone.md) | `POST /v1/people/enrich` | [docs](https://api.contactout.com/#people-enrich-api) |
| [Enrich Person With Work Email](actions/enrich-person-with-work-email.md) | `POST /v1/people/enrich` | [docs](https://api.contactout.com/#people-enrich-api) |
| [Get API Usage Stats](actions/get-api-usage-stats.md) | `GET /v1/stats` | [docs](https://api.contactout.com/#api-usage-stats) |
| [Get Batch Email Verification Job](actions/get-batch-email-verification-job.md) | `GET /v1/email/verify/batch/:job_uuid` | [docs](https://api.contactout.com/#bulk) |
| [Get Decision Makers By Company Name](actions/get-decision-makers-by-company-name.md) | `GET /v1/people/decision-makers` | [docs](https://api.contactout.com/#decision-makers-api) |
| [Get Decision Makers By Domain](actions/get-decision-makers-by-domain.md) | `GET /v1/people/decision-makers` | [docs](https://api.contactout.com/#decision-makers-api) |
| [Get Decision Makers By LinkedIn Company URL](actions/get-decision-makers-by-linked-in-company-url.md) | `GET /v1/people/decision-makers` | [docs](https://api.contactout.com/#decision-makers-api) |
| [Get Decision Makers With Contact Reveal](actions/get-decision-makers-with-contact-reveal.md) | `GET /v1/people/decision-makers` | [docs](https://api.contactout.com/#decision-makers-api) |
| [Get LinkedIn Contact Info](actions/get-linked-in-contact-info.md) | `GET /v1/people/linkedin` | [docs](https://api.contactout.com/#from-linkedin-profile) |
| [Get LinkedIn Contact Info With Phone](actions/get-linked-in-contact-info-with-phone.md) | `GET /v1/people/linkedin` | [docs](https://api.contactout.com/#from-linkedin-profile) |
| [Get Person By Email](actions/get-person-by-email.md) | `GET /v1/people/person` | [docs](https://api.contactout.com/#email-to-linkedin-api) |
| [Queue Batch Email Verification](actions/queue-batch-email-verification.md) | `POST /v1/email/verify/batch` | [docs](https://api.contactout.com/#bulk) |
| [Search Companies](actions/search-companies.md) | `POST /v1/company/search` | [docs](https://api.contactout.com/#company-search-api) |
| [Search Companies HQ Only](actions/search-companies-hq-only.md) | `POST /v1/company/search` | [docs](https://api.contactout.com/#company-search-api) |
| [Search People](actions/search-people.md) | `POST /v1/people/search` | [docs](https://api.contactout.com/#people-search-api) |
| [Search People By Company](actions/search-people-by-company.md) | `POST /v1/people/search` | [docs](https://api.contactout.com/#people-search-api) |
| [Search People By Job Title](actions/search-people-by-job-title.md) | `POST /v1/people/search` | [docs](https://api.contactout.com/#people-search-api) |
| [Search People With Contact Reveal](actions/search-people-with-contact-reveal.md) | `POST /v1/people/search` | [docs](https://api.contactout.com/#people-search-api) |
| [Verify Email](actions/verify-email.md) | `GET /v1/email/verify` | [docs](https://api.contactout.com/#single) |
