# White Swan: Native API Reference

A consolidated summary of White Swan's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.whiteswan.io/partner-knowledge-base/api-documentation
- **API base URL:** `https://app.whiteswan.io/api/1.1/wf`

## Authentication

### API Key

Connect White Swan with your partner API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud White Swan App` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Case Party](actions/add-case-party.md) | `POST /invite_case_party` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/add-case-party) |
| [Create Pre-Fill Information](actions/create-pre-fill-information.md) | `POST /new_prefill_info` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/create-pre-fill-information) |
| [List Account Users](actions/list-account-users.md) | `POST /user` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/account-user-s) |
| [List Earnings Events](actions/list-earnings-events.md) | `POST /earnings_event` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/earnings-event-s) |
| [List Personal Plans](actions/list-personal-plans.md) | `POST /personal_plan` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/personal-plan-s) |
| [List Plan Requests](actions/list-plan-requests.md) | `POST /plan_requests` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/plan-request-s) |
| [List Referred Clients](actions/list-referred-clients.md) | `POST /client` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/referred-client-s) |
| [Policy Search](actions/policy-search.md) | `POST /policy_search` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/policy-search) |
| [Start Application](actions/start-application.md) | `POST /start_application` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/start-application) |
| [Start Personal Plan Request](actions/start-personal-plan-request.md) | `POST /new_request` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/start-personal-plan-request) |
| [Submit Complete Plan Request](actions/submit-complete-plan-request.md) | `POST /complete_request` | [docs](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/submit-complete-plan-request) |
