# CodeSubmit: Native API Reference

A consolidated summary of CodeSubmit's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.codesubmit.io/integrations/api
- **API base URL:** `https://app.codesubmit.io`

## Authentication

### API Key

Use a provider-generated CodeSubmit API key from the Integrations settings page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://www.codesubmit.io/integrations/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Invite Users](actions/bulk-invite-users.md) | `POST /api/company/users/invite_bulk` | [docs](https://www.codesubmit.io/integrations/api) |
| [Cancel Subscription](actions/cancel-subscription.md) | `DELETE /api/company/payment/subscription` | [docs](https://www.codesubmit.io/integrations/api) |
| [Change My Password](actions/change-my-password.md) | `POST /api/external/me/password` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create Assessment](actions/create-assessment.md) | `POST /api/external/tests` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create Bytes Assessment](actions/create-bytes-assessment.md) | `POST /api/external/tests/byte` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create CodePair Session](actions/create-code-pair-session.md) | `POST /api/external/codepair` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create CodePair Template](actions/create-code-pair-template.md) | `POST /api/external/codepair/templates` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create Integration](actions/create-integration.md) | `POST /api/company/integrations` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create Talent Boost](actions/create-talent-boost.md) | `POST /api/company/talent/boosts` | [docs](https://www.codesubmit.io/integrations/api) |
| [Create Talent Job](actions/create-talent-job.md) | `POST /api/company/talent/jobs` | [docs](https://www.codesubmit.io/integrations/api) |
| [Delete Integration](actions/delete-integration.md) | `DELETE /api/company/integrations` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Applicants Stats](actions/get-applicants-stats.md) | `GET /api/external/stats?stats=applicants` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Billing Customer](actions/get-billing-customer.md) | `GET /api/company/payment/customer` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Candidate Invite Trend](actions/get-candidate-invite-trend.md) | `GET /api/external/stats?stats=candidates_invited_period` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Candidates Completed Stats](actions/get-candidates-completed-stats.md) | `GET /api/external/stats?stats=candidates_completed` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Candidates Invited Stats](actions/get-candidates-invited-stats.md) | `GET /api/external/stats?stats=candidates_invited` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /api/company/settings` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Current User](actions/get-current-user.md) | `GET /api/external/me` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get My Settings](actions/get-my-settings.md) | `GET /api/external/me/settings` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Subscription](actions/get-subscription.md) | `GET /api/company/payment/subscription` | [docs](https://www.codesubmit.io/integrations/api) |
| [Get Talent Settings](actions/get-talent-settings.md) | `GET /api/company/talent` | [docs](https://www.codesubmit.io/integrations/api) |
| [Invite Candidate](actions/invite-candidate.md) | `POST /api/external/candidates` | [docs](https://www.codesubmit.io/integrations/api) |
| [Invite Company User](actions/invite-company-user.md) | `POST /api/company/users` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Assessments](actions/list-assessments.md) | `GET /api/external/tests` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Candidates](actions/list-candidates.md) | `GET /api/external/candidates` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Company Users](actions/list-company-users.md) | `GET /api/company/users` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Integrations](actions/list-integrations.md) | `GET /api/company/integrations` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Invoices](actions/list-invoices.md) | `GET /api/company/payment/invoices` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Library Challenges](actions/list-library-challenges.md) | `GET /api/external/library?page_size=100` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Quick Create Languages](actions/list-quick-create-languages.md) | `GET /api/external/codepair/quick-create/languages` | [docs](https://www.codesubmit.io/integrations/api) |
| [List Talent Jobs](actions/list-talent-jobs.md) | `GET /api/company/talent/jobs` | [docs](https://www.codesubmit.io/integrations/api) |
| [Open Billing Portal](actions/open-billing-portal.md) | `POST /api/company/payment/portal` | [docs](https://www.codesubmit.io/integrations/api) |
| [Quick Create CodePair](actions/quick-create-code-pair.md) | `POST /api/external/codepair/quick-create` | [docs](https://www.codesubmit.io/integrations/api) |
| [Request Library Challenge](actions/request-library-challenge.md) | `POST /api/external/library_templates/request_challenge` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update Company](actions/update-company.md) | `PUT /api/company` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update Company Settings](actions/update-company-settings.md) | `PUT /api/company/settings` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update Integration](actions/update-integration.md) | `PUT /api/company/integrations` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update My Settings](actions/update-my-settings.md) | `PUT /api/external/me/settings` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update Subscription](actions/update-subscription.md) | `PUT /api/company/payment/subscription` | [docs](https://www.codesubmit.io/integrations/api) |
| [Update Talent Settings](actions/update-talent-settings.md) | `PUT /api/company/talent` | [docs](https://www.codesubmit.io/integrations/api) |
